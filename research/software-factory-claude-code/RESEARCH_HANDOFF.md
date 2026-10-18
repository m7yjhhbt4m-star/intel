# Research handoff: Claude Code Software Factory

> **Prepared by:** ChatGPT (OpenAI GPT-6)  
> **Research date:** 2026-10-18  
> **Status:** Source-verified static review; not installed, executed, or runtime-tested  
> **Purpose:** Give future AI assistants enough provenance, architecture, findings, and next steps to evaluate this project without repeating the initial research.

## Executive summary

The Software Factory is a small **Claude Code-specific agent workflow**, not a standalone application or a general-purpose autonomous coding platform. A user invokes `/factory <feature>`; a Claude Code session coordinates a spec-writing agent, a builder, four parallel reviewers, and an approver. The agents communicate through Markdown files and per-job JSON state. The builder works in a separate Git worktree and branch. The final approver either allows a local merge to `main` or escalates the job for human review.

The source is promising as a readable prototype: its workflow is visible, the work is separated into small agents, changes are tested against explicit acceptance criteria, and it uses Git worktrees to isolate feature branches. However, it should **not be installed unchanged into the Sovereign Media Engine (SME)** or treated as a proven production workflow.

The highest-priority findings are:

1. **Dashboard exposure:** the README's `python3 -m http.server` command serves job records without authentication and, by default, listens on all network interfaces. Job records may contain code, implementation details, test logs, or sensitive project context.
2. **Approval policy:** an agent can authorize a change to merge automatically. Human escalation is limited to listed risk categories and cases the approver recognizes. For an early SME trial, require a human merge decision.
3. **Prompt-only isolation:** agents are instructed to stay in their assigned worktree and write only designated files, but those rules are not equivalent to OS-level isolation. Several agents have shell access.
4. **Dashboard reliability:** it discovers jobs by parsing the HTML directory listing produced by a web server. It can fail as a whole if a job directory is visible before its `job.json` exists or while JSON is being rewritten.
5. **Docker compatibility:** the factory is not itself Dockerized. The orchestrator depends on Claude Code skills, subagent definitions, Claude Code tool semantics, Git, worktrees, and (for UI checks) `agent-browser`. Putting the app under development in Docker does not automatically containerize the factory or make it compatible with arbitrary open-source models.
6. **Incomplete validation:** two example jobs are present, but I did not execute the workflow. The examples do not establish that parallel jobs, revision rounds, failed setup, recovery, or conflict paths work reliably.

**Recommended direction:** preserve the original source as a reference, document the findings, then run a small isolated proof of concept on the MacBook Pro. Do not adapt the SME repository or NAS until the proof of concept passes explicit tests.

---

## 1. Provenance and source verification

### Primary source

- Repository: [zazencodes/zazencodes-season-3](https://github.com/zazencodes/zazencodes-season-3)
- Project path: [src/software-factory-claude-code](https://github.com/zazencodes/zazencodes-season-3/tree/7f8a22b/src/software-factory-claude-code)
- Reported source snapshot: commit `7f8a22b`, dated 2026-10-02 in the source report supplied by the user.
- Upstream repository's latest commit observed during this research: `555467c365e6750278efba09349369109f62f65f`, dated 2026-10-07, with message “Update README with software factory video and thumbnail.”
- Verification note: the current upstream `main` tree returned the same tree identifiers for the factory's `.claude` and `factory` directories and the same hashes for the main factory files as the supplied 2026-10-02 snapshot. The later repository commit was a README change; no newer factory implementation was observed in the checked tree.

### Files independently checked against GitHub

- `README.md`
- `BUILD_PROMPT.md`
- `.claude/skills/factory/SKILL.md`
- All seven agent definitions under `.claude/agents/` (their paths and tree entries were checked; the supplied report provided their full text)
- `factory/backlog.md`
- `factory/dashboard.html` (read directly from the source; 23,827 bytes)
- Example job `001-blog-reading-time`: `decision.md`, `round-1/review-security.md`, and `round-1/review-code.md`
- Example job `002-not-found-page`: `decision.md`, `round-1/review-security.md`, and `round-1/review-code.md`
- The example-job tree, including each job's spec, build record, JSON state, and four review files.

### Scope and limitations

This is a **static source review**. I did not clone or run the repository, invoke Claude Code, run its agents, execute its dashboard in a browser, or reproduce its example changes. The conclusions below distinguish directly observed implementation details from risks inferred by reading the source. A future reviewer should rerun this inspection against the upstream default branch before implementation.

The source repository's inspected root listing did not show a `LICENSE` file. That does not by itself settle copyright or reuse rights. **Do not vendor or redistribute the original source code into another repository until its applicable license or permission is confirmed.** This handoff documents and links to the source rather than copying the implementation.

---

## 2. What the factory contains

### Workflow

```text
/factory <feature>
    |
    v
spec-writer (Opus)
    |
    v
builder (Opus; separate worktree and factory/<job-id> branch)
    |
    +---- security reviewer (Opus) ----+
    +---- UX reviewer (Sonnet) --------+
    +---- UI reviewer (Sonnet) --------+--> wait for all four
    +---- code reviewer (Sonnet) ------+          |
                                                 +-- any CHANGES --> resume builder
                                                 |                  and review again
                                                 |                  (up to 2 resumes)
                                                 v
                                         approver (Opus)
                                           /          \
                                      APPROVE        ESCALATE
                                         |              |
                                  local merge to main  needs-human
```

The normal path involves seven named agent roles: one spec writer, one builder, four reviewers, and one approver. Reviewer jobs are launched in parallel, and the orchestrator is instructed to wait for all four before deciding whether to resume the builder.

### Main files

- `.claude/skills/factory/SKILL.md`: orchestrator procedure and slash-command behavior.
- `.claude/agents/spec-writer.md`: writes the job spec and acceptance criteria.
- `.claude/agents/builder.md`: implements the spec in the feature worktree, tests it, commits changes, and writes the build record.
- `.claude/agents/reviewer-security.md`: security-focused review.
- `.claude/agents/reviewer-ux.md`: user flow, states, accessibility, and UX review.
- `.claude/agents/reviewer-ui.md`: visual consistency and responsive UI review.
- `.claude/agents/reviewer-code.md`: correctness, simplicity, conventions, docs, and validation.
- `.claude/agents/approver.md`: final decision to approve or escalate.
- `factory/dashboard.html`: self-contained visual dashboard.
- `factory/backlog.md`: queue consumed by `/factory next`.
- `factory/jobs/<job-id>/`: runtime state, including `job.json`, spec, build log, reviews, rework notes, and decision.
- `../<repo>-factory/<job-id>/`: worktree for the job's branch, outside the main checkout.

### Important difference from the original build prompt

The original `BUILD_PROMPT.md` describes one shared `factory/board.json`. The implemented factory has evolved: **each job has its own `factory/jobs/<job-id>/job.json`**, and the dashboard reads each job directory. The README explicitly says the factory now uses per-job JSON and Git worktrees so multiple jobs can run concurrently. Do not use `board.json` as the implementation contract; the current skill and per-job `job.json` design are the operative design in the inspected source.

### Commands documented by the project

- `/factory <feature>`: start a feature job.
- `/factory next`: claim and start the first unchecked backlog item.
- `/factory approve <job-id>`: merge a job in `needs-human`.
- `/factory rework <job-id> <note>`: send an escalated job back for further work.
- Dashboard per README: run `python3 -m http.server` from the `factory/` directory and open `http://localhost:8000/dashboard.html`.

### What the examples demonstrate

- `001-blog-reading-time`: the builder and four reviewers report success, but the approver escalates because the change touches a prerender script considered deploy-related. The decision record explains the specific human decision needed.
- `002-not-found-page`: the approver allows a small static 404-page change to merge locally.

These are useful examples of the approval distinction. They are not evidence that the whole workflow has been runtime-tested across failure and concurrency cases.

---

## 3. Technical critique

Severity here is a research assessment, not a claim that a vulnerability has been exploited.

### HIGH — Dashboard may expose job data to the local network

The README starts Python's built-in HTTP server with `python3 -m http.server`. Unless a bind address is supplied, Python's server listens on all interfaces. The dashboard recursively reads job directories and renders Markdown files, and the server can also serve any other file under its root. There is no authentication layer.

**Impact:** anyone able to reach the server port may be able to view job specs, build logs, review notes, and other files in the served tree. These records can reveal source paths, implementation details, operational assumptions, or secrets accidentally written into logs.

**Minimum safe local command:**

```bash
cd factory
python3 -m http.server --bind 127.0.0.1 8000
```

For Docker, publish the port only on the host loopback interface, for example `127.0.0.1:8000:8000`, and separately ensure the container server is reachable inside the container. Do not expose this dashboard through a router, public reverse proxy, or NAS port-forward without an explicit access-control design.

### HIGH — Auto-merge is a policy choice, not a hard safety boundary

The approver can write `APPROVE`, after which the orchestrator merges the branch into the local `main` checkout without a separate human review. Escalation is required for specified categories such as money, access/identity, deploy/CI/hosting, schema migrations, production writes, email, dependencies, and product assumptions.

**Risk:** the model must recognize every relevant category and correctly judge whether the change is safe. A category can be missed, or a change may have effects not covered by the checklist. Passing reviews do not prove that a change is safe.

**Recommendation for SME:** for the first proof of concept, make human approval mandatory before every merge. Only consider automatic local merges after tests demonstrate reliable behavior and the allowed scope is explicitly defined. Keep NAS changes, production data, secrets, deployment, permissions, and destructive operations out of the autonomous path.

### HIGH — Agent write boundaries are mostly instructions

The agent files say each agent writes only its designated file, and the builder must work only in its job worktree. However, agents have tools such as `Bash`, `Write`, and (for the builder) `Edit`. The workflow's own text is not an operating-system boundary that prevents a mistaken command from editing the main checkout or accessing files outside the intended worktree.

Git worktrees reduce branch collision; they do not sandbox shell commands or make malicious or mistaken instructions harmless.

**Recommendation:** use Claude Code's permission controls and a disposable development container with only the required repository and test dependencies mounted. Avoid bypassing permission prompts. Keep credentials, NAS mounts, personal archives, production databases, and other unrelated files outside the agent's accessible environment. Verify the actual permissions and mount boundaries before running agents.

### HIGH — This is not a drop-in open-source-model orchestrator

The workflow relies on Claude Code-specific conventions: a `SKILL.md`, custom subagent frontmatter, tool names, named subagent sessions, and resuming the same builder through `SendMessage`. Merely replacing the `opus`/`sonnet` labels with a local model name does not provide the same orchestration runtime.

**Implication for the MacBook proof of concept:** decide whether Claude Code itself will orchestrate the factory, or whether the project must be ported to a different open-source agent framework. These are different projects. An API-compatible gateway may be an option only if the exact Claude Code features and target model are supported and tested; compatibility should not be assumed.

### MEDIUM — Dashboard depends on a server's directory-listing HTML

The dashboard calls `fetch('jobs/')`, parses the returned HTML for directory links, and then fetches each `job.json`. It recursively parses directory listings again to find Markdown files.

This works with the Python HTTP server documented by the README. It is not a general static-web assumption: common web servers may disable directory listing, and a Docker image using a different server may return a 403/404 or a different page.

**Recommendation:** for the first test, use the documented server and test the dashboard as supplied. If Docker is the target, either retain the expected directory-index behavior deliberately or replace it with a small explicit job-index endpoint/manifest. Avoid a larger rewrite until the prototype is measured.

### MEDIUM — One incomplete job directory can break the whole board poll

The orchestrator creates a job directory and then writes `job.json`. The dashboard enumerates all directories and uses `Promise.all` to fetch and parse every job's JSON. If the dashboard polls between directory creation and the JSON write, or if JSON is temporarily incomplete during a rewrite, one failure rejects the entire load and the board reports an error.

The same concern applies when `job.json` is rewritten on every stage transition.

**Recommendation:** make state writes atomic (write a temporary file and rename it), and have the dashboard handle a missing or malformed job file per job rather than failing the whole board. Add a test that polls during job creation and state updates.

### MEDIUM — Backlog claims can be stranded

`/factory next` changes the first unchecked item to a claimed state, then starts a job and later replaces the marker with the job ID. If the session stops between those steps, the item can remain marked as claimed without an obvious automatic recovery mechanism.

**Recommendation:** add a documented recovery procedure or a claim record with a job ID, timestamp, and explicit stale-claim handling. Do not add a complicated queue system unless real use demonstrates that it is needed.

### MEDIUM — Conflicting instruction about who writes decisions

The skill says the orchestrator never writes decisions and that agents write their own files. Later, when revision rounds are exhausted, the skill instructs the orchestrator itself to write `decision.md`.

**Impact:** the workflow contradicts its own ownership rule. This may not break the normal path, but it creates uncertainty about which component owns the decision record.

**Recommendation:** make one rule authoritative: either allow the orchestrator to write this specific mechanical escalation record and document the exception, or spawn the approver/decision writer for that path too.

### MEDIUM — The tested behavior is not broad enough to establish reliability

The repository contains two example jobs. One was escalated and one was approved. The supplied records include review and build evidence, but I did not run the factory. The visible examples do not establish that the following cases work:

- a reviewer fails to produce a file or writes an invalid verdict;
- the builder reports `STATUS: BLOCKED`;
- the first review requests changes and the builder is resumed;
- the second resume is exhausted;
- two jobs claim IDs and run concurrently;
- one job merges while another branch is in progress;
- a merge conflict or worktree cleanup failure occurs;
- the dashboard polls while a job folder or JSON file is being created;
- a stale backlog claim is recovered;
- browser checks run without touching real services or real user accounts.

**Recommendation:** use a short, explicit test matrix before trusting the workflow for real project work.

### MEDIUM — Local merge does not push to GitHub

The skill explicitly says **“Never push.”** A successful merge updates the local `main` checkout only. It does not update the remote GitHub repository.

This is a deliberate conservative choice, but the operator must know that a merged job is not necessarily published. Keep remote pushes and pull-request creation as separate human-controlled steps in the proof of concept.

### MEDIUM — UI checks add a separate runtime dependency and risk surface

The README asks the user to install `agent-browser`. Builder and UI reviewers launch a development server and use a browser session; the UX reviewer also browses the app. The agent instructions tell reviewers not to sign in or submit forms because the app might connect to real services, which is a useful safeguard.

**Risks:** the CLI is an extra dependency, its version is not pinned in the described setup, and browser sessions may still encounter real data/services if the local development configuration is not isolated.

**Recommendation:** pin and document the tested version; use a test-only configuration and fake/sandbox services; make browser testing opt-in for jobs that actually change the UI; verify cleanup of sessions and servers after failures.

### MEDIUM — Agent count and model allocation may be expensive

The normal workflow invokes Opus for spec-writing, building, security review, and approval, plus three Sonnet reviewers. Any revision can repeat the builder and all four reviews. The workflow does not describe a token budget, maximum changed-file scope, or a strategy for avoiding redundant reviews.

This provides multiple perspectives, but it can create significant token use and repeated reading for small changes.

**Recommendation:** measure tokens and elapsed time on a small sample. Preserve mandatory security review, but consider whether UX/UI browser reviews are needed for a non-UI change. Do not remove reviewers simply to reduce cost until the test results show which reviews add value.

### LOWER — Some runtime conventions need to be made explicit

- Job folders are runtime state and the README instructs users to gitignore `factory/jobs/`; preserve this distinction between source template and runtime records.
- The worktree is placed next to the repository. A Docker setup must mount the parent directory (or intentionally choose another layout) so the main checkout and sibling worktrees refer to the same host files and survive container recreation.
- Setup instructions in `AGENTS.md` or `CLAUDE.md` are executed in a fresh worktree. Treat those commands as executable project code; inspect them and use a disposable test project first.
- The dashboard and factory should be tested with the exact versions of Git, Claude Code, Python, and `agent-browser` intended for the target machine.

---

## 4. Fit for the user's MacBook Pro / Docker-first plan

### What can run where

| Component | Role | Initial recommendation |
|---|---|---|
| Claude Code orchestrator | Reads the skill, creates jobs, launches/resumes agents | Use the native Claude Code runtime first unless there is a specific reason to containerize it. Confirm authentication and tool permissions. |
| Target application and dependencies | The project being modified and tested | Run in Docker where practical, with test-only services and no production credentials. |
| Git worktrees | Isolate each feature branch | Ensure the repository's parent directory is mounted or otherwise accessible so sibling worktrees are real, persistent host paths. |
| Dashboard | Read-only view of job state | Run the documented local server first; bind to loopback. Containerize only after verifying the directory-listing dependency. |
| `agent-browser` | Browser-based UI checks | Install and pin a known version in the chosen runtime; use isolated test services and browser sessions. |
| Open-source/local model | Alternative to Claude models | Not a drop-in replacement. Select a compatible agent runtime and port/test the orchestration separately if local-model support is a requirement. |

### Minimal proof of concept

Use a throwaway test repository with a simple app, a passing test command, and no credentials or production integrations.

1. **Source and permission check:** confirm the upstream revision, Claude Code version, agent tool syntax, Git version, and local permission settings.
2. **Installation only:** add the factory files to the throwaway repository; do not copy them into SME yet. Confirm the skill appears and can be invoked.
3. **Simple non-UI feature:** run one small change through spec, build, reviews, approval, and local merge. Keep a human in the approval loop.
4. **Revision-path test:** introduce a harmless, deliberately testable issue that triggers a review change. Verify the same builder resumes and all four reviewers wait/finish as required.
5. **Escalation-path test:** confirm an escalated job stays available for inspection and can be approved or reworked deliberately.
6. **Dashboard test:** start it on loopback, create a job while it is polling, and confirm missing/partial state does not hide all jobs. Do not expose it on the LAN.
7. **Worktree and Docker test:** verify the worktree path is persistent, both main and feature checkout see expected files, and deleting/recreating a container does not destroy job work.
8. **Cost and recovery test:** record model usage, time, number of tool calls, and failure recovery. Check concurrent job IDs and merge-conflict behavior.
9. **Only after all tests pass:** decide whether to adapt it for SME, with SME-specific gates and no NAS access.

### Acceptance criteria for the proof of concept

- A one-line feature request creates a unique job folder and branch/worktree.
- The spec contains observable acceptance criteria and real project validation commands.
- The builder changes only the feature worktree and leaves it clean after committing.
- All four review files exist before the orchestrator makes a review-round decision.
- A `CHANGES` review causes a builder revision and a new review round, within the configured limit.
- Invalid/missing agent output is handled as an explicit error, not silently treated as success.
- `APPROVE` and `ESCALATE` are parsed only from the exact expected first line.
- No branch merges without the required human approval during the proof of concept.
- Dashboard failures are isolated to a job where possible and cannot expose the dashboard beyond localhost.
- No credentials, NAS mounts, archive data, production data, or deployment access are available to the test agents.
- The workflow's token usage, runtime, and all failure cases are recorded.

---

## 5. Recommendations for an eventual SME adaptation

Do not make these changes yet; treat them as design requirements for a later, authorized adaptation.

1. **Human approval first.** The factory should not autonomously merge into SME's primary branch during initial trials.
2. **No NAS access.** Agents must operate only in a disposable MacBook test workspace. No NAS mounts or credentials.
3. **No deployment or production changes.** Deployment, CI, hosting, schema, credentials, production writes, dependencies, and permission changes require explicit human review.
4. **Explicit scope limits.** Every job must state permitted paths and prohibited paths. Stop and ask if the feature exceeds scope.
5. **Provenance.** Preserve the feature request, spec, branch/commit IDs, all reviews, test commands/results, decision, and any human override.
6. **Fail closed.** Missing, malformed, or contradictory state must stop the job. It must never be interpreted as a pass.
7. **Recoverable state.** Make job-state writes atomic and backlog claims recoverable.
8. **Isolated tests.** Use test databases, fake integrations, and disposable data. No real account logins or production endpoints in browser tests.
9. **Measured token use.** Track cost and repeated context. Keep accuracy and independent review as priorities, but avoid invoking irrelevant agents.
10. **Separate research from implementation.** This report is research only; it does not authorize changes to the SME repo or NAS.

---

## 6. Open questions for the next research pass

- What license or explicit permission governs reuse of the upstream source?
- What exact Claude Code version and current subagent/skill semantics are required by the project?
- Does the skill execute correctly on the target MacBook Pro without changing the host environment unexpectedly?
- Can the factory operate safely with the intended Docker boundary and sibling worktrees?
- What happens when a reviewer, builder, browser, or merge operation fails at each stage?
- How much model usage does a small feature consume, including a revision cycle?
- Is the dashboard's directory-index approach worth keeping, or should the Docker proof of concept use an explicit manifest?
- If open-source models are required, which agent runtime will replace Claude Code-specific orchestration? That is a separate comparison and implementation decision.

---

## 7. Sources

### Primary source code

- [Original factory directory at the reported source snapshot](https://github.com/zazencodes/zazencodes-season-3/tree/7f8a22b/src/software-factory-claude-code)
- [Factory README](https://github.com/zazencodes/zazencodes-season-3/blob/7f8a22b/src/software-factory-claude-code/README.md)
- [Orchestrator skill](https://github.com/zazencodes/zazencodes-season-3/blob/7f8a22b/src/software-factory-claude-code/.claude/skills/factory/SKILL.md)
- [Dashboard source](https://github.com/zazencodes/zazencodes-season-3/blob/7f8a22b/src/software-factory-claude-code/factory/dashboard.html)
- [Original build prompt](https://github.com/zazencodes/zazencodes-season-3/blob/7f8a22b/src/software-factory-claude-code/BUILD_PROMPT.md)
- [Example 001 decision](https://github.com/zazencodes/zazencodes-season-3/blob/7f8a22b/src/software-factory-claude-code/factory/jobs/001-blog-reading-time/decision.md)
- [Example 002 decision](https://github.com/zazencodes/zazencodes-season-3/blob/7f8a22b/src/software-factory-claude-code/factory/jobs/002-not-found-page/decision.md)

### Official documentation consulted for context

- [Claude Code setup](https://docs.anthropic.com/en/docs/claude-code/getting-started)
- [Claude Code CLI reference](https://docs.anthropic.com/en/docs/claude-code/cli-usage)
- [Claude Code security](https://docs.anthropic.com/en/docs/claude-code/security)
- [Claude Code LLM gateway configuration](https://docs.anthropic.com/en/docs/claude-code/llm-gateway)

Official documentation is contextual guidance, not evidence that this particular factory has passed runtime tests.

---

## Research status

**Verified:** source paths and snapshot; current upstream factory tree comparison; dashboard implementation; selected example decisions and reviews; major workflow and safety implications.

**Not verified:** runtime behavior; successful installation; end-to-end agent execution; actual token cost; Docker operation; current license/permission status; local-model compatibility.

**Next action:** conduct the isolated MacBook Pro proof of concept only after deciding the desired Claude Code versus open-source orchestration path. Keep SME and NAS out of scope until that test is complete.
