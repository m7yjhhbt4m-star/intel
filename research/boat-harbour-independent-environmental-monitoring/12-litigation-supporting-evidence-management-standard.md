# Litigation-Supporting Evidence Management Standard
**Boat Harbour / A’se’k Independent Environmental Monitoring Research**

- **Document:** 12
- **Version:** 1.0 — draft for legal, technical and rights-holder governance review
- **Prepared:** 23 November 2026
- **Repository:** `m7yjhhbt4m-star/intel`
- **Applies to:** the Boat Harbour / A’se’k independent environmental monitoring research stream and any future documentary, digital, field, laboratory or expert material added to it.

> **Important limitation:** This is a proposed evidence-management procedure, not legal advice, a litigation protocol approved by counsel, an expert opinion, or a certification of admissibility. No database can guarantee that a record will be admitted in court. Counsel must identify the actual forum, causes of action, procedural rules, disclosure duties, limitation periods, privilege issues and any court orders before evidence is collected or used for a proceeding.

## 1. Purpose and governing principle

The database is to be maintained as a **traceable research and evidence-management system** capable of being audited by independent counsel, scientists, forensic specialists and, where appropriate, a court. Every material factual proposition must be traceable to an identified source and precise location in that source. Every physical sample or original digital record intended to support a factual allegation must have a documented acquisition and custody history.

The standard is deliberately stricter than ordinary desk research. It does not convert a source into proof merely because the source is official, Indigenous-authored, scientific, peer-reviewed or publicly available. Authorship, authenticity, reliability, completeness, relevance, hearsay issues, expert qualification, methodology and admissibility are separate questions.

## 2. Immediate repository and information-security finding

**The GitHub repository `m7yjhhbt4m-star/intel` was confirmed on 23 November 2026 to have public visibility.** It is therefore not an evidence vault and must be treated as a public publication surface.

Until its visibility and access model are deliberately changed by the repository owner:

- Do not upload original evidence files containing personal information, confidential correspondence, health information, privileged material, witness details, private contact information, protected Indigenous knowledge, sensitive harvesting locations, archaeological locations, burial locations, or other restricted cultural information.
- Do not upload raw field notebooks, unredacted interview records, audio/video of community members, medical records, or laboratory records containing personal identifiers.
- Do not place legal advice, counsel instructions, litigation strategy, draft affidavits, expert-retainer communications or privileged analysis in this public repository.
- The public repository may hold a carefully reviewed index, source metadata, public links, non-sensitive analysis, claim references and procedural documentation.
- Original files and restricted derivatives must be held in a separate, access-controlled evidence store with versioning, audit logs, retention controls and, where feasible, write-once/read-many (WORM) retention or object lock.

No repository visibility change or evidence-vault deployment is authorized by this document. Those are separate owner decisions.

## 3. Applicable law and standards — jurisdiction must be confirmed

The following are relevant reference points, not a complete legal opinion:

1. **Canada Evidence Act, section 2:** Part I applies to criminal proceedings and civil proceedings or other matters within Parliament’s jurisdiction. It is not a universal code for every provincial proceeding.
2. **Canada Evidence Act, sections 31.1–31.7:** address authentication and the best-evidence rule for electronic documents. Section 31.1 places the burden of authenticating an electronic document on the person seeking to admit it. Section 31.2 addresses integrity of the electronic-document system; section 31.7 confirms that these provisions do not displace other admissibility rules except authentication and best evidence.
3. **Federal Courts Rules:** if the matter is a Federal Court application, the current Rules and applicable practice directions govern. Rule 52.2 requires an expert affidavit or statement to set out the proposed evidence, qualifications and the expert’s certificate agreeing to the Code of Conduct for Expert Witnesses. Rule 52.2(2) permits exclusion for non-compliance. Part 5 (Rules 300–319) governs applications, including judicial review. Affidavit evidence and tribunal-record rules must be reviewed in the actual proceeding.
4. **Federal Court judicial-review guide:** the Court’s guide identifies section 18.1 of the Federal Courts Act and Part 5 of the Federal Courts Rules as relevant to judicial review of federal boards, commissions and tribunals. It also describes the record, affidavits, supporting documents and cross-examination process. The guide is not a substitute for the Rules or legal advice.
5. **Environment Canada, The Inspector’s Field Sampling Manual, 2nd ed. (2005):** provides federal guidance on sampling planning, legal sampling, continuity/chain of custody, sample labels, seals, notebooks, transport, laboratory handling and QA/QC. It expressly states that legislation takes precedence and that protocols may need to be adapted by subject-matter experts.
6. **ISO/IEC 17025:** laboratory accreditation is relevant only when the laboratory is accredited for the particular method and analyte/matrix combination. Accreditation alone does not prove that a particular sample was collected correctly or that its result is reliable.

**Required legal gate:** before a litigation use is contemplated, counsel must produce a short written applicability note identifying the intended forum (Federal Court, Nova Scotia court, tribunal, regulatory enforcement process or other), the governing evidence/procedure rules, the record available on judicial review, preservation/disclosure obligations, limitation issues, confidentiality/privilege restrictions and the status of any existing proceeding. Do not assume the same rules govern every possible case.

## 4. Evidence classes and status labels

Every source and every material claim must carry a status. Do not use a single vague label such as “verified.”

### 4.1 Source acquisition status

| Code | Status | Minimum meaning |
|---|---|---|
| A0 | Original acquired and preserved | Exact original bytes obtained from the identified source, stored in the controlled evidence vault, SHA-256 calculated, acquisition log completed, and preservation copy verified |
| A1 | Original acquired; preservation incomplete | Exact original bytes obtained, but one or more preservation controls (second copy, signed manifest, independent verification, WORM retention) remain outstanding |
| B | Official-source full-content review | Official registry or publisher provides the complete document and it has been read, but the original binary has not been acquired and hashed in the evidence vault |
| C | Partial content reviewed | Only selected pages, excerpts, OCR/search results, executive summary or partial text have been reviewed |
| D | Metadata/index only | Existence, author, date, title or attachment identity located, but the document content has not been reviewed |
| E | Secondary account | News, commentary, third-party summary or other non-primary source; original source still required where material |

A0/A1 describe acquisition and preservation, not truth or admissibility. B/C/D/E must never be presented as if the original binary has been preserved.

### 4.2 Claim status

- **Directly documented:** the cited source expressly states the proposition. This does not mean the proposition is independently true.
- **Independently corroborated:** a second genuinely independent source supports the same material fact; independence and common-source risks are documented.
- **Disputed:** a material source contradicts or contests the proposition.
- **Inferred:** derived from identified facts by a stated reasoning process; assumptions are listed.
- **Unverified:** not enough source material to decide.
- **Not established:** the reviewed evidence does not establish the proposition. This is not proof that the proposition is false.
- **Refuted:** reliable evidence directly contradicts the proposition; the basis and scope of refutation must be stated.

Use attribution in every report: “PLFN submits…”, “IAAC records…”, “the proponent reports…”, “the laboratory measured…”, “the court held…”. Never silently convert a party’s assertion into a database fact.

## 5. Source intake and digital chain of custody

### 5.1 Before acquisition

For each source, create an immutable Source ID before analysis. Record:

- Source ID and source family/related-document IDs.
- Exact title, original filename, author/creator, submitting party, recipient, document date, submission date and registry reference.
- Issuing body or custodian and whether it is a primary record, copy, transcript, summary, extract, derivative or secondary account.
- Exact source URL and registry/project identifier.
- Retrieval date and time in UTC, retrieval operator, method/tool and software/version.
- Access conditions, copyright/re-use terms, confidentiality, privacy and Indigenous knowledge restrictions.
- Whether the source appears complete; page count, attachments, appendices, exhibits and referenced materials that are absent.
- Any digital signature, visible signature, seal, metadata, document properties, revision marks or redactions.

### 5.2 Acquire and preserve

1. Acquire the original file directly from the official registry, issuing authority, custodian or documented provider where possible.
2. Preserve the exact bytes as received. Do not print-to-PDF, re-save, OCR, optimize, redact, rename internally, normalize metadata or otherwise alter the original preservation copy.
3. Record byte size and calculate SHA-256 immediately after acquisition. Where feasible, independently calculate the hash a second time and verify that it matches.
4. Preserve the acquisition receipt, download log, source-page metadata, URL, UTC time, relevant HTTP response metadata/headers and screenshots or a WARC capture where lawful and technically available.
5. Place the original in a restricted evidence vault with versioning, access logging, backup and write-protection. Maintain at least two independently controlled copies. A checksum alone does not make storage immutable.
6. Create a separate working copy for OCR, text extraction, redaction, annotation, translation, conversion or analysis. Hash each derivative and record its parent Source ID and transformation history.
7. Record every access, transfer, export, restoration, migration, integrity check and authorized disclosure in the custody/access log.
8. If the original cannot be obtained, record why, what alternative representation was used, what the browser or registry displayed, and the limits of that representation. Do not assign A0/A1.

### 5.3 Hashes and repository history

- SHA-256 is the minimum file-integrity hash for original files and derivatives.
- Store the hash in a signed or otherwise independently protected manifest that identifies the exact file and its storage location.
- Git commit history is useful for the history of research notes and metadata; it is not a substitute for a controlled evidence vault, a source-file hash, a digital-signature validation or an independently protected audit log.
- The public GitHub repository must not be treated as WORM storage. Repository administrators can change history, permissions and contents.
- No silent overwrite or deletion is permitted. Corrections are new versions with a reason, author, timestamp, affected records and prior-version reference. Preserve the prior version.
- Any future migration to a new repository or database must preserve Source IDs, hashes, version history, custody logs and cross-references.

## 6. Document review and claim extraction

### 6.1 Review procedure

For each material document:

1. Confirm document identity and acquisition status.
2. Review the entire document, including cover, author/submitter details, dates, signature pages, contents, appendices, exhibits, footnotes, references, redactions and attachments.
3. Record pages that are missing, illegible, corrupted, duplicated, out of sequence or not supplied.
4. Compare OCR/text extraction against the page image. Correct extraction errors only in a derivative; retain the uncorrected extraction and log corrections.
5. Record material passages with precise page/paragraph/table/figure/footnote identifiers. Browser line numbers are a convenience, not a permanent legal pinpoint.
6. Distinguish the author's own statements from quotations, summaries, citations to other documents and hearsay within the document.
7. Identify assumptions, methods, data sources, limitations, conflicts, contrary evidence and requested actions.
8. For high-impact documents, require a second reviewer to independently check the source identity, material extracts, citations and claim coding. Record both reviewers and disagreements.
9. Do not call a document “fully reviewed” until all pages and attachments within the defined scope have been checked.

### 6.2 Claim ledger

Every material proposition used in a report must have a unique Claim ID and at least:

- exact proposition, written neutrally;
- claim type (historical, legal position, technical, scientific, health, community testimony, regulatory, project status, inference);
- source ID and exact pinpoint;
- source author's role/perspective;
- whether the text is direct, quoted, summarized or inferred;
- claim status from section 4.2;
- corroborating and contradicting sources;
- assumptions and unresolved questions;
- reviewer and review date;
- whether expert or counsel review is required;
- reports/documents that rely on the claim.

A claim with no pinpoint source is not ready for inclusion in a factual report.

### 6.3 Competing positions and negative evidence

- Preserve contradictory, exculpatory, adverse and inconvenient material with the same care as supportive material.
- Do not delete a source because it is superseded; mark its temporal status and what it was superseded by.
- Record whether a source is independent or repeats another source.
- Do not treat several summaries of one underlying report as independent corroboration.
- Distinguish absence of a record from proof that an event did not occur.
- Maintain an issues register for missing records, unanswered information requests and failed retrieval attempts.

## 7. Indigenous rights-holder and knowledge governance

This research must not appropriate, flatten or expose Indigenous knowledge.

- Attribute each position to its actual authoring Nation, organization, individual, study team or government. “Indigenous view” is not an acceptable generic source label.
- Keep PLFN's own submissions separate from IAAC's interpretation, the proponent's account and other Mi’kmaq communities' submissions.
- Public availability of a document does not automatically grant permission to extract, map, republish or redistribute sensitive Indigenous knowledge.
- Do not place confidential traditional-use locations, sacred/culturally sensitive places, burial locations, medicinal knowledge, interview recordings or restricted community data in the public repository.
- Follow the knowledge-holder's and rights-holder's applicable protocols, permissions, access conditions and publication decisions. Where these are unknown, restrict access and do not publish the content.
- Do not infer consent from participation in an environmental assessment, consultation meeting, funded study, public submission or receipt of a report.
- The appropriate rights-holder must determine who may authorize access, interpretation, secondary use, retention, mapping and publication of its knowledge. This cannot be decided by the research team.
- A governance review must precede any new interviews, community health data collection, traditional-use mapping or use of Indigenous knowledge in models.

## 8. Environmental field evidence and laboratory chain of custody

No field sampling is to be represented as litigation-quality evidence unless a qualified sampling lead has approved a project- and analyte-specific Sampling and Analysis Plan (SAP), Quality Assurance Project Plan (QAPP) and legal-sampling procedure before fieldwork begins.

### 8.1 Pre-field controls

The SAP/QAPP must identify:

- the question and decision the sample is intended to address;
- conceptual site model, source–pathway–receptor hypotheses and competing hypotheses;
- sample locations, coordinates, coordinate reference system, station rationale, depths, matrices, tide/stage and timing;
- analytes, analytical methods, detection/reporting limits, method interferences and data-quality objectives;
- sample containers, cleaning/certification, preservatives, filtration requirements, holding times, storage temperature and shipping;
- field instruments, serial numbers, calibration/verification and maintenance;
- decontamination procedures and cross-contamination controls;
- field blanks, equipment blanks, trip blanks where applicable, duplicates, matrix spikes, reference materials, split samples and frequency rationale;
- laboratory identity and current ISO/IEC 17025 accreditation scope for the specific method and matrix;
- sample volume, subsampling, compositing rules, retention and disposal;
- safety plan, permits, access permissions, Indigenous monitoring/participation arrangements and cultural protocols;
- deviation, non-conformance, resampling and escalation procedures.

The SAP/QAPP must be technically reviewed by an independent qualified professional before sampling.

### 8.2 At collection

For every sample, record contemporaneously:

- unique sample ID, project ID, station ID and sample type;
- sampler names and roles; all witnesses present;
- date/time with time zone, coordinates, datum, GPS device/accuracy, depth, tidal stage, weather and field conditions;
- matrix, collection method, equipment and decontamination steps;
- bottle/container ID and lot/certificate, preservative, filtration and field measurements;
- photographs/video of site, sample, labels and seals, with original files preserved;
- field observations, unusual conditions, deviations and rejected/invalid samples;
- custody seal number and sample condition at sealing.

Use permanent, unique, waterproof labels. Labels, field notebook, sample submission form and chain-of-custody form must cross-reference the same sample ID.

### 8.3 Custody, transport and laboratory receipt

- Seal each sample or approved sample group with uniquely numbered tamper-evident seals.
- Keep samples in direct possession, in view, or secured in a locked container. Limit handlers.
- Record every transfer: relinquishing and receiving persons, date/time/time zone, location, purpose, seal condition and signatures.
- Record cooler/container ID, seal numbers, temperature, packing materials, courier, waybill/tracking, dispatch and delivery times.
- Notify the laboratory before shipment and confirm receipt, seal condition, temperature, sample condition, holding-time compliance and any discrepancies.
- The laboratory must document sample receipt, custody, condition, storage, preparation, analysis, quality-control results, analyst, method/version, instrument identifiers and any deviations.
- Retain raw instrument output, chromatograms/spectra, calibration records, batch QC, calculations, data qualifiers, certificates and signed reports—not only the final concentration table.
- Preserve split samples and retained aliquots where scientifically feasible and safe, with custody and storage conditions recorded.
- Any broken seal, missing custody signature, exceeded holding time, temperature excursion, mislabeled sample, failed blank or other deviation must be logged and assessed. Never silently repair the record. Flag affected results and obtain expert review.

### 8.4 Laboratory quality

Accreditation must be checked against the actual laboratory, facility, method, analyte and matrix at the date of analysis. A laboratory's general statement that it is ISO/IEC 17025 accredited is insufficient if the relevant test is outside its scope. Verify proficiency testing, method validation, reporting limits, uncertainty, blank contamination, recoveries and data qualifiers. Independent split-sample testing should be considered for high-consequence analytes and disputed results.

### 8.5 Field notes and corrections

Field notes must be contemporaneous, dated, attributable and retained in original form. Do not erase, overwrite, backdate or reconstruct notes as though contemporaneous. Correct an error with a single-line strike-through that leaves the original legible, then add the correction, initials, date/time and reason. Later recollection must be recorded as a later memorandum with its actual date and basis.

## 9. Photographic, video, drone, sensor and geospatial records

- Preserve original camera/drone/sensor files, memory-card structure where relevant, metadata and device logs.
- Hash originals before editing or transcoding.
- Preserve original timestamps and document clock settings, time-zone offsets, GPS source, coordinate system, sensor calibration, firmware, software and processing settings.
- Do not rely on a screenshot, exported still, compressed social-media upload or edited video when the original file is available.
- Maintain a derivative history for stabilization, cropping, colour correction, georeferencing, mosaicking, orthorectification, classification, AI enhancement and annotation.
- Keep raw observations, calibrated measurements, processed products and interpretive maps as separate linked records.
- For drone or remote-sensing claims, document ground-control/check points, accuracy, weather, sensor geometry, water conditions, validation samples and known detection limits.
- AI-generated descriptions, object detections, transcripts or summaries are leads, not primary evidence. Human reviewers must verify them against original media.

## 10. Witness, interview, translation and community testimony records

- Obtain informed consent and the necessary permissions before recording or collecting testimony.
- Record who conducted the interview, who was present, date/time/location, method, language, interpreter identity and any limits on use.
- Preserve the original recording and an unaltered transcript/translation derivative separately.
- Identify verbatim quotation, paraphrase, interpreter rendering, interviewer summary and later recollection as different record types.
- Give participants a defined opportunity to correct factual transcription errors where appropriate, while preserving the original and logging amendments.
- Do not convert a participant's lived experience or testimony into a medical diagnosis, causal finding or technical measurement.
- Apply rights-holder governance and privacy controls before storage, access, analysis or publication.

## 11. Expert evidence and technical independence

The research team may identify questions and assemble source material; it must not present itself as a qualified expert witness.

Any expert report intended for legal use should be prepared and signed by the qualified expert who takes responsibility for it. At minimum, the expert record should disclose:

- qualifications, experience, relevant licences and proposed area of expertise;
- instructions, scope and questions addressed;
- all material data and documents relied upon, including contrary material;
- methods, standards, models, software and versions;
- assumptions, exclusions, uncertainty, detection limits and sensitivity analyses;
- calculations and enough working material to permit reproduction;
- alternative explanations considered and why they were accepted or rejected;
- conflicts, funding, relationships and limits on independence;
- conclusions separated from facts, assumptions and opinions;
- limitations and additional work needed.

For Federal Court use, counsel and the expert must check current Federal Courts Rules rule 52.2 and the Code of Conduct for Expert Witnesses. The expert's duty is to assist the Court impartially; the expert is not an advocate. Do not draft an expert opinion and attribute it to a scientist who has not independently reviewed and adopted it.

## 12. AI and automation controls

- AI may help locate, classify, transcribe, compare and summarize records, but it is not a witness, expert, laboratory, source custodian or legal decision-maker.
- Never treat an AI-generated summary as the source. Every material claim must point to the underlying original record and pinpoint.
- Preserve the prompt/model/tool/version and transformation log for AI-derived work where it materially affects evidence interpretation.
- Human review is mandatory for legal, technical, health, Indigenous knowledge and environmental conclusions.
- AI may not silently correct OCR, resolve contradictions, invent missing metadata, infer a chain of custody, fill gaps with assumptions or assign legal conclusions.
- Any AI-generated output that cannot be reproduced or checked against source material must be excluded from the evidentiary claim ledger.

## 13. Legal hold, disclosure, privacy and privilege

When litigation is reasonably contemplated or counsel issues a hold:

1. Counsel must define the scope and custodians.
2. Suspend routine deletion, rotation, overwriting and disposal for relevant material.
3. Preserve original devices, accounts, email, messages, field notebooks, lab files, photographs, video, drone data, backups and metadata within scope.
4. Record hold notices, recipients, acknowledgement, exceptions and compliance checks.
5. Keep privileged legal advice and counsel work product in a counsel-controlled restricted workspace; do not label material privileged without counsel's direction.
6. Maintain a disclosure log and record redactions with reason, authorizer and unredacted source reference.
7. Do not destroy physical samples or records subject to a hold without written authorization from counsel and the responsible custodian.

Publicly available information is not automatically free of privacy, confidentiality, copyright, cultural-governance or procedural restrictions.

## 14. Review, audit and release gates

A source or claim may not be promoted to “reviewed for legal use” unless all applicable gates pass:

- [ ] source identity and author/submitter confirmed;
- [ ] original file acquired or acquisition limitation explicitly recorded;
- [ ] hash and custody controls complete for A0/A1 records;
- [ ] completeness, attachments, page sequence and redactions checked;
- [ ] OCR/text extraction checked against page images;
- [ ] precise pinpoints recorded;
- [ ] direct assertion distinguished from quotation, hearsay, inference and summary;
- [ ] corroborating and contradictory evidence searched;
- [ ] independent second review completed for material claims;
- [ ] legal/privilege/privacy/Indigenous governance restrictions checked;
- [ ] expert review obtained where a technical or scientific opinion is required;
- [ ] report wording accurately reflects source status and limitations;
- [ ] version, reviewer, date and approvals recorded.

The database must preserve a full audit trail of changes, access, review, correction, export and disclosure. A periodic independent audit should test a sample of source files, hashes, claim pinpoints, chain-of-custody entries, permissions and backup restoration.

## 15. Current implementation status — 23 November 2026

**This standard is proposed, not yet implemented as an operational evidence-management system.**

Confirmed in this review:

- The GitHub repository is public.
- Original PLFN documents are accessible through the official IAAC registry and their complete PDF text is available in the browser review.
- The source files have not yet been acquired as binary originals into a controlled evidence vault and SHA-256 hashed in this work session. Their current acquisition classification is B, not A0/A1.
- The repository does not yet contain a deployed immutable evidence vault, signed hash manifest, append-only custody log, role-based access control, WORM retention or independent backup verification.
- No field samples have been collected under this proposed protocol in this research work.
- No legal counsel has approved this standard and no expert has adopted the research conclusions as expert opinion.

Do not state that the database is court-ready, legally certified, admissible, or that chain of custody has been established for source files until the relevant controls have actually been implemented and independently audited.

## 16. Primary standards and references

- [Canada Evidence Act, R.S.C. 1985, c. C-5](https://laws-lois.justice.gc.ca/eng/acts/C-5/FullText.html) — especially ss. 2 and 31.1–31.7.
- [Federal Courts Rules, SOR/98-106](https://laws-lois.justice.gc.ca/eng/regulations/SOR-98-106/FullText.html) — especially Part 5, rule 52.2 and the Code of Conduct for Expert Witnesses.
- [Federal Court — How to file an Application for Judicial Review](https://www.fct-cf.gc.ca/en/pages/representing-yourself/practice-guides/how-to-file-an-application-for-judicial-review) — procedural guide; check current Rules and counsel advice.
- [Environment Canada, The Inspector’s Field Sampling Manual, 2nd ed. (2005)](https://publications.gc.ca/collections/Collection-R/En40-498-2005-1E.pdf) — sample planning, legal sampling and chain-of-custody guidance. It is guidance, not a substitute for current project-specific SOPs or legislation.
- [Canadian Association for Laboratory Accreditation (CALA) — Accreditation](https://cala.ca/accreditation) — scope-specific laboratory accreditation information and ISO/IEC 17025 programme information.

## 17. Approval required before operational use

This draft must be reviewed and approved by:
1. litigation counsel familiar with the intended forum and applicable procedural rules;
2. an environmental sampling/QA professional with relevant matrices and analytes experience;
3. a digital-evidence/records-management specialist;
4. PLFN or the appropriate knowledge-holder authority for any rights-holder data, Indigenous knowledge, interview or cultural material to be collected or used.

Until those approvals occur, use this as a conservative research control framework, not as a representation that all legal requirements have been met.
