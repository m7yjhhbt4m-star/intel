# Primary Record Acquisition — Outstanding Groundwater Documents and Spatial Source Files
**Document:** 17  
**Version:** 1.0 — 23 November 2026  
**Purpose:** Track the original documents and native-format datasets required to complete the groundwater evidence review and build a dated spatial atlas. This is an acquisition log, not a claim that files have been downloaded.

## 1. Acquisition status definitions

- **A0 — Located:** source identity or registry record located; binary not acquired.
- **A1 — Binary acquired:** original bytes downloaded; filename, byte size and SHA-256 recorded.
- **A2 — Preserved:** original binary stored read-only in controlled evidence storage with provenance and chain-of-custody record.
- **B — Text reviewed:** full or partial browser-rendered text examined; original binary not acquired/hashed.
- **C — Partial review:** excerpt, executive summary, index or secondary catalogue summary only.
- **D — Not obtained:** source identified but no original content acquired.
- **E — Unavailable/blocked:** access or retrieval attempt failed; reason and date recorded.

A source can have more than one status dimension, for example **B + E** (text reviewed, original binary download blocked). Do not call a source “acquired” when only a web-rendered text view or search snippet was read.

## 2. Original groundwater records

| Source ID | Original record | Exact source locator | Current status | Required next action |
|---|---|---|---|---|
| BH-089 | AECOM, *Drilling and Hydraulic Testing Program, Boat Harbour, NS*, Project No. 60446127, 2016 (also cited as Boat Harbour Hydrogeology Assessment) | EIS Appendix Z, identified at p.208; https://iaac-aeic.gc.ca/050/documents/p80164/137897E.pdf | A0/D: title and Appendix Z location confirmed; full report and native files not retrieved | Obtain full report, figures, appendices, pumping-test raw data, model files, calibration, well logs and coordinates |
| BH-095 | GHD, *Well Field Evaluation Report*, 2018 | EIS Appendix Z, identified at p.300; same Appendix Z PDF above | A0/D: source identity and location confirmed; full report not independently retrieved | Obtain full report, wellfield capture-zone model, input files, model run outputs, maps, pumping assumptions and uncertainty |
| BH-088 | Dillon Consulting, *Pictou Landing IR24 2010 Groundwater Monitoring Program — Final Report*, August 2011 | Cited in EIS Volume V reference list and Hive IR82 analysis; https://iaac-aeic.gc.ca/050/documents/p80164/137223E.pdf (EIS Volume V reference context) | A0/D: exact title/date identified; report itself not retrieved | Obtain full report, all appendices, well logs, water levels, chemistry tables, lab certificates, field sheets and maps |
| BH-091 | Dillon Consulting, *Pictou Landing IR24 Groundwater Exploration Study — Phase II*, January 2003 | Cited in EIS Volume V reference list; https://iaac-aeic.gc.ca/050/documents/p80164/137223E.pdf | A0/D: exact title/date identified; original report not retrieved | Obtain complete report and the underlying wellfield exploration records, maps, pumping tests and construction logs |
| BH-090 | GHD, *Greenhouse Gas Mitigation Assessment*, June 2018 | Cited in GHD 2022 draft GHG memorandum | A0/D: source lead only | Obtain full report and calculation workbook; preserve draft/final status and scenario assumptions |
| BH-092 | 2019 groundwater/containment-cell monitoring report cited by EXP technical review | EXP Services review submitted by PLFN | A0/D: title and exact registry record not confirmed | Identify exact title, author, date, monitoring period and obtain original report and lab certificates |
| BH-093 | GHD, *Sampling and Analysis of Dredge Spoils Report* | Cited by EXP Services technical review | A0/D: source lead only | Identify registry entry and retrieve report, sample inventory, locations, methods and lab certificates |

### Why the missing originals matter
The 2020 EIS Volume IV says monitoring wells occur in three areas: BHETF, the new off-peninsula PLFN wellfield and the old PLFN wellfield. It reports 30 wells installed in the 2018 Phase II ESA, seven additional wells in the Supplemental Phase II ESA, and 50 site wells in total. These are EIS-reported counts, not an independently reconciled well inventory. The 2016 AECOM and 2018 GHD interpretations differ on hydraulic connection/capture-zone behaviour; the raw records and model files are needed to independently test the interpretations.

## 3. Newer regulatory and project records

| Source ID | Record | Source locator | Current status | Required next action |
|---|---|---|---|---|
| BH-081 / BH-049 / BH-011 | Build Nova Scotia, *Boat Harbour Remediation Project 2025 Annual Report to the Impact Assessment Agency of Canada*, registry document 74 / file 166307E.pdf, dated 30 March 2026 | Official registry search: https://iaac-aeic.gc.ca/050/evaluations/exploration?culture=en-CA&projDocs=80164; registry record resolves to https://iaac-aeic.gc.ca/050/evaluations/document/166307 | A0 + C + E: official identity/date confirmed; secondary catalogue abstract reviewed; official PDF body not read; direct retrieval timed out | Obtain official PDF, preserve/hash, review all 25 pages and all condition-by-condition tables/appendices; compare against Decision Statement and project updates |
| BH-094 | Industrial Approval No. 94-032 and all amendments/replacement approvals for Boat Harbour | Referred to in BGC review and other project records | D: not obtained | Obtain certified complete instrument history, schedules, maps, monitoring conditions, amendments, compliance records and closure obligations |
| New source lead | Approved EMP/PEPP and current groundwater/surface-water monitoring plans | EIS Appendix B and final/provincial approval framework | D: current approved versions not verified | Obtain approval stamps, effective dates, revisions, monitoring locations, frequencies, analytes, trigger levels and reporting obligations |
| New source lead | 2025–2026 monitoring and compliance records | Proponent, provincial regulator, IAAC | D: no raw current records obtained in this pass | Request field sheets, lab certificates, electronic data deliverables, QA/QC, water-level series, incidents and annual reports |
| New source lead | Official Federal Court judicial-review record and subsequent orders/status | PLFN judicial review concerning federal approval | D: court record not examined in this acquisition pass | Obtain docket, pleadings, hearing date, orders and reasons; do not use media reports as authoritative court status |

### Important status qualification
A secondary catalogue summary of the 2025 Annual Report states that the project remained in a pre-construction phase during the report's 2025 reporting period because of a judicial review filed by PLFN, and that the Alternative Site Advisory Committee was established. This is a lead only until the official 25-page report is acquired and read. It does not establish what happened after 31 December 2025.

## 4. Spatial data acquisition

| Dataset | Native format to request | Known source / status | Main limitations |
|---|---|---|---|
| 2016 AGRG topo-bathymetric lidar | LAZ/LAS point cloud, GeoTIFF DEM/DSM, orthophoto, shapefiles/GeoPackage, model grids and raw ADCP CSV | AGRG/NSCC 2017 report reviewed; native deliverables not obtained | Written permission required before sharing underlying data; report states AGRG/NSCC owns data and processing IP |
| Historical aerial photos | Original scanned TIFF/JPEG plus frame index, flight line, date/time, camera/focal metadata and scan resolution | GeoNOVA DataLocator and Aerial Photography Library identified; Boat Harbour frame inventory not queried | Some film may not yet be scanned; georeferencing/orthorectification must be documented |
| 2024/2025 orthophotos | Original GeoTIFF tiles plus tile index, image acquisition date, resolution, CRS and licence | GeoNOVA June 2026 release identified; exact Boat Harbour coverage unconfirmed | Do not assume all eastern Nova Scotia tiles cover the project site |
| Provincial LiDAR | Original LAZ/LAS; derived GeoTIFF DEM, DSM, hillshade, CHM and intensity; tile metadata | Elevation Explorer identified; site-specific tiles not queried | Confirm acquisition year, classification, resolution, horizontal and vertical datums |
| Hydrography | SHP, GDB or GeoPackage; network metadata and flow direction | Nova Scotia Hydrographic Network identified as provincial authoritative inland-water dataset | Current network is not a historic shoreline record |
| Canadian Hydrographic Service | Original sounding data, multibeam grids, charts and survey metadata | Cited in 2017 AGRG report as 5 m multibeam source | Need exact survey IDs, coverage, acquisition date, vertical datum and licence |
| Groundwater well inventory | CSV/XLSX plus original well logs/PDF, coordinates and construction diagrams | EIS and IR response summaries reviewed; complete reconciled inventory not obtained | Coordinate systems, screened intervals and identifiers may vary among sources |
| Groundwater chemistry | Original lab EDD CSV/XLSX, certificates PDF, field sheets, QA/QC and sample coordinates | EIS summary only | Do not create interpolated plumes from incomplete sample points |
| ADCP and tide records | Native CSV/ASCII time series, instrument metadata, calibration, deployment/recovery logs | 2017 AGRG report documents 11 Aug–13 Sep 2016 deployment | Report figures are not a substitute for raw time series |
| Model outputs | Native model project, grid, boundary conditions, input data, run logs and outputs | 2017 AGRG model described; 2016 groundwater model cited but not retrieved | Model outputs must remain separate from observations |

## 5. Formats for the documentary evidence database

Preserve and embed the following separately:

1. **Original source:** original PDF, TIFF, LAZ, LAS, GeoTIFF, CSV, XLSX, SHP/GDB or native model files, unchanged.
2. **Text extraction:** UTF-8 text or Markdown, page markers retained; OCR confidence and extraction tool/version recorded.
3. **Tables:** CSV for flat tables; XLSX only where multi-sheet structure is material. Retain original units, qualifiers, footnotes and page/table locators.
4. **Spatial vectors:** GeoPackage preferred for normalized working layers; retain original shapefiles/geodatabases unchanged.
5. **Rasters:** GeoTIFF with CRS, vertical datum, resolution, NoData and acquisition metadata; never silently resample the preserved original.
6. **Point clouds:** original LAZ/LAS with classification and CRS metadata.
7. **Time series:** CSV/Parquet with timezone, timestamp precision, station ID, units, sensor and QA flags.
8. **Database ingest:** PostGIS geometry plus JSONB provenance/metadata; store source-file object references and SHA-256 hashes.
9. **Map derivatives:** GeoPackage/GeoJSON for vectors and GeoTIFF/COG for raster derivatives; each derivative receives its own hash and processing record.

Never make a PDF-only copy and discard the native data. Never treat OCR output, extracted CSV or digitized map features as the original record.

## 6. Retrieval blockers encountered in this pass

- The connected Firecrawl service reported insufficient available credits and explicitly declined the requested batch retrieval. No retry was made.
- Direct binary downloads from the working container failed because external DNS/network resolution was unavailable in that runtime.
- The official IAAC registry links for the 230 MB EIS Appendix Z and the 2025 Annual Report were identified, but browser retrieval timed out.
- The browser-rendered text of the 2017 AGRG report was available and examined, but this did not deliver the PDF bytes or native spatial datasets.

**Consequently, no original document binaries or native spatial datasets were saved or SHA-256 hashed in this pass.** This is an acquisition failure, not evidence that the documents do not exist. The source links and retrieval targets are recorded above so the next retrieval can resume without repeating discovery.

## 7. Immediate retrieval order
1. Official 2025 Annual Report PDF (25 pages) and all appendices.
2. EIS Appendix Z complete PDF (230 MB), then extract AECOM 2016 and GHD 2018 originals and figures from their exact page locations.
3. Dillon 2011 and 2003 groundwater reports and raw wellfield records.
4. Current Industrial Approval 94-032, amendments, approved EMP/PEPP and provincial monitoring records.
5. 2016 AGRG/NSCC native spatial deliverables and written data-use permission.
6. DataLocator historical photo frame inventory and selected scans.
7. Exact 2024 orthophoto and LiDAR tile coverage for the project footprint.
8. CHS multibeam source data and metadata.
9. Reconciled well/sample station inventories, lab EDDs, certificates and QA/QC.
10. Official judicial-review docket and all later project/monitoring records.

## 8. Research references
- EIS Volume IV: https://iaac-aeic.gc.ca/050/documents/p80164/137222E.pdf
- EIS Volume V: https://iaac-aeic.gc.ca/050/documents/p80164/137223E.pdf
- EIS Appendix Z: https://iaac-aeic.gc.ca/050/documents/p80164/137897E.pdf
- IAAC-67 consolidated response: https://iaac-aeic.gc.ca/050/documents/p80164/144782E.pdf
- Hive Engineering IR82 analysis: https://iaac-aeic.gc.ca/050/documents/p80164/155835E.pdf
- 2025 Annual Report registry: https://iaac-aeic.gc.ca/050/evaluations/exploration?culture=en-CA&projDocs=80164
- AGRG/NSCC 2017 report: https://www.nscc.ca/appliedresearch/docs/geomatics-psc-ns-lands-finalreport-mar2017.pdf
- Nova Scotia DataLocator: https://nsgi.novascotia.ca/datalocator/
- Elevation Explorer: https://nsgi.novascotia.ca/datalocator/elevation


## 9. Provincial Boat Harbour monitoring order and the underlying station map

| Source ID | Record | Exact source locator | Current status | Required next action |
|---|---|---|---|---|
| BH-101 | Nova Scotia Environment and Climate Change, Ministerial Order MO-60007, issued 28 May 2021 to Nova Scotia Lands Inc.; groundwater/surface-water requirements effective 1 June 2021 | https://novascotia.ca/nse/issues/docs/Nova-Scotia-Lands-Ministerial-Order-June-01-2021.pdf | B + E: full browser-rendered text reviewed, original PDF binary not acquired/hashed. Order text identifies eight BHETF wells, quarterly frequency, analytes, 15-year record retention and annual reporting by 1 April | Obtain original PDF bytes and hash; confirm current legal status and all amendments/written approvals; obtain annual reports and quarterly monitoring records 2021–2026 |
| BH-102 | Dillon Consulting Limited, File 18-7281-2000, *Boat Harbour Effluent Treatment System – 2018 Monitoring Program*, March 2019 | Cited in MO-60007 Appendix B Table 3 as source of Figure 3-1 showing monitoring locations | A0/D: exact title, file number, date and map citation identified; report and Figure 3-1 not obtained | Obtain full report, map, well coordinates, construction details, field methods, lab results and certificates; confirm whether this is the same report referenced in the earlier EXP review before merging with BH-092 |

### MO-60007 obligations that make the missing records especially important
Condition 37 of MO-60007 requires an annual groundwater/surface-water report by 1 April following the monitoring year. Required contents include current and historical static water levels, gradients and flow direction, current and historical groundwater chemistry, laboratory certificates, spatial and temporal trend analysis, and adverse-impact identification/recommendations. Conditions 36–38 require at least 15-year retention of BHETF groundwater-well records and qualified-professional oversight.

The order's Appendix B, Table 3 identifies MW15-1S, MW15-1D, MW15-2S, MW15-2D, MW15-3S, MW15-3D, MW15-4S and MW15-5S for quarterly groundwater sampling. This BHETF network must be kept distinct from PLFN production wells PW9/PW10 and the off-peninsula wellfield. The order does not establish that the PLFN production aquifer was monitored by these BHETF wells.

**Required records request:** all annual reports due under condition 37 from 2021 onward, all underlying quarterly sample events and lab EDDs/certificates, water-level readings, well inspection/maintenance records, Figure 3-1 and well construction data, plus every Department authorization changing the network, analytes or frequency. Ask the Department to confirm whether MO-60007 remains operative and whether any later order, approval, written authorization or closure/decommissioning instrument superseded it.



## 10. EIS wellfield map and 1995–2019 groundwater series

EIS Volume IV (BH-038) contains Figures 7.1-12 through 7.1-16:
- Figure 7.1-12: containment-cell monitoring network.
- Figure 7.1-13: containment-cell groundwater elevations versus time.
- Figure 7.1-14: PLFN wellfield water-supply and monitoring-well locations, dated 17 August 2020, NAD 1983 CSRS UTM Zone 20N.
- Figures 7.1-15 and 7.1-16: PLFN overburden and shallow-bedrock groundwater elevations versus time.

The EIS states containment-cell monitoring-well groundwater elevations were typically measured quarterly from 1995 through 2019. The EIS figures and tables are available as part of the reviewed EIS Volume IV, but the raw time-stamped readings, original coordinates, well construction records, measuring-point elevations and source GIS project remain outstanding.

**Required extraction:** preserve the EIS figure pages as page-image assets, extract each displayed hydrograph/table with page/figure locators, and separately request the underlying electronic time-series from the proponent/regulator. If the map is digitized, store digitized coordinates as approximate/derived geometry with control points, transformation method and residual error; do not relabel them as surveyed coordinates.


## 11. Alternate retrieval route: official EIS volumes and provincial orders

The standalone Appendix Z attachment could not be retrieved through the registry's 230 MB PDF endpoint. The alternate route was to retrieve the EIS volumes separately, use their internal references and figure content, and retrieve the provincial orders as individual smaller PDFs.

### 11.1 EIS Volume IV — recovered through direct PDF indexing

- Official PDF: https://iaac-aeic.gc.ca/050/documents/p80164/137222E.pdf
- Full text is available through the web PDF index.
- Relevant material: pages 7-44 to 7-73, Figure 7.1-14 (PLFN wellfield map), Figures 7.1-17 to 7.1-24 (GHD 2018 PLFN wellfield hydrographs), Tables 7.1-20 and 7.1-21 (shallow and deep bedrock wellfield elevation ranges), and discussion of 1995–2019 historical monitoring.
- Figure title blocks identify GHD job 11148275-25 and 6 June 2018 for the wellfield hydrographs. Hydrographs cover several screened depth intervals and show manual/continuous water elevations alongside precipitation.
- This provides a useful evidence extract while the standalone GHD report and original logger files remain outstanding.

### 11.2 EIS Volume V — recovered as a bibliographic source

- Official PDF: https://iaac-aeic.gc.ca/050/documents/p80164/137223E.pdf
- Its reference list confirms the exact titles/dates of AECOM 2016, Dillon 2003, Dillon 2011, and the separate Dillon 2018/2019 sludge-disposal-cell monitoring reports.
- This is bibliographic confirmation, not a substitute for the underlying reports.

### 11.3 Appendix Z — identified but large-file retrieval failed

- Official registry page: https://iaac-aeic.gc.ca/050/evaluations/proj/80164/document/137959
- Registry attachment filename: 137897E.pdf; size listed as 230 MB.
- Registry fetch timed out. Direct download through the working container also failed.
- The request should now be split: ask IAAC/Build Nova Scotia for AECOM 2016, GHD 2018 and relevant Dillon reports as individual attachments rather than requesting the combined 230 MB PDF. Ask for native spreadsheets, model files, well construction logs and GIS layers separately.

### 11.4 Smaller official provincial orders recovered

- MO-55774, 29 January 2020, Northern Pulp: https://novascotia.ca/nse/issues/docs/55774-Ministerial-Order-NPNS-January-2020.pdf
- MO-60003, 14 May 2020, Northern Pulp: https://novascotia.ca/nse/issues/docs/MO-60003-NPNSC.pdf
- MO-60007, 28 May 2021, Nova Scotia Lands: https://novascotia.ca/nse/issues/docs/Nova-Scotia-Lands-Ministerial-Order-June-01-2021.pdf

All three were reviewed in full browser-rendered text. Their original binaries have not yet been downloaded to the controlled evidence vault or hashed. Their chronology and conditions are summarized in Document 15, Section 10.

### 11.5 2025 annual report retrieval status

- Registry search page: https://iaac-aeic.gc.ca/050/evaluations/exploration?culture=en-CA&projDocs=80164
- Listing: reference 74, document 166307E.pdf, dated 30 March 2026.
- Registry attachment page and direct PDF fetch timed out; guessed direct path was not accessible.
- Canada Commons lists a 25-page copy/catalogue, but access was not confirmed. Treat as not acquired until a downloadable official or authenticated copy is obtained and hashed.


## 12. Project-hosted technical reference library located

A more useful acquisition lead was found inside the EIS itself. EIS Volume V, Section 10.2 (PDF pages 10-15 to 10-16) explicitly states that selected references are available for download from the former Boat Harbour Remediation Project website:

**Project resource index cited by the EIS:** https://novascotia.ca/boatharbour/resources.asp

The EIS assigns numbered download entries. The key groundwater records are:
- **Item 01:** AECOM (2016), *Drilling and Hydraulic Testing Program Boat Harbour, NS*, Project No. 60446127.
- **Item 05:** Dillon Consulting (January 2003), *Pictou Landing IR24 Groundwater Exploration Study – Phase II*.
- **Item 06:** Dillon Consulting (August 2011), *Pictou Landing IR24 2010 Groundwater Monitoring Program – Final Report*.
- **Item 07:** Dillon Consulting (March 2019), *Sludge Disposal Cell – BHETF – 2018 Monitoring Report*.
- **Item 08:** Dillon Consulting (March 2020), *Sludge Disposal Cell – BHETF – 2019 Monitoring Report*.

The EIS identifies the resource page and item numbers, but the legacy ASP resource page itself was not accessible to the current retrieval browser. Do not infer the underlying file URLs from the item numbers. The exact link targets must be recovered from the page source, an archived copy, or a current provincial records custodian.

This is materially better than an unbounded search: it provides an official, contemporaneous index of the exact original documents and a numbered route by which the proponent intended them to be obtained.

### 12.1 Separate report identities — do not merge

The following are distinct and should have separate source IDs and separate original-file records:
- PLFN wellfield history: Dillon 2003 Phase II exploration (BH-091).
- PLFN wellfield monitoring: Dillon 2010 program / August 2011 final report (BH-088).
- BHETF sludge disposal cell monitoring: 2018 monitoring report (BH-092).
- BHETF sludge disposal cell monitoring: 2019 monitoring report (BH-109).
- BHETF broader groundwater/surface-water station network: Dillon March 2019 *2018 Monitoring Program*, File 18-7281-2000 (BH-102).

### 12.2 What can be used now from the EIS itself

EIS Volume IV contains selected material from the GHD 2018 PLFN Well Field Evaluation (job 11148275-25), including:
- Figures 7.1-17 to 7.1-24, with hydrographs for multiple depth intervals and manual/continuous measurements.
- Figure title blocks showing 6 June 2018.
- Water elevation tables for PLFN shallow and bedrock monitoring wells.
- A discussion of the historical and operational water-level patterns.

This is suitable as a page-cited secondary extraction from the EIS, but the chart values must not be silently treated as raw electronic measurements. Any digitization from the hydrograph images must be marked as graph-derived, with pixel-to-axis calibration, digitizer identity, resolution and uncertainty. Request the native logger data and GHD source spreadsheets before presenting a numerical time series as measured data.


## 13. Current official project resource page — new acquisition route

The current project website exposes direct document links and has proven more useful than trying to retrieve the old 230 MB Appendix Z bundle.

**Official resources page:** https://boatharbourproject.buildns.ca/resources

Documents successfully opened and text-reviewed:
- *Boat Harbour Remediation Project 2025 Annual Report* (25 pages), direct PDF: https://buildns.ca/wp-content/uploads/2026/03/2025-Annual-Report-to-IAAC-Final.pdf — source BH-110.
- GHD, *Design Requirements Document*, Report No. 4, Project 11148275, 12 September 2017, 37 pages: https://boatharbourproject.buildns.ca/s/Design-Requirements-Document.pdf — source BH-112.
- GHD, *Remedial Option Decision Document*, Report No. 5, Project 11148275, 1 May 2018, 406 pages: https://boatharbourproject.buildns.ca/s/Remedial-Options-Decision-Document_compressed.pdf — source BH-111.

Other resources listed on the same official page:
- Laboratory Treatability Study — link target surfaced as a Squarespace static PDF, but this retrieval browser could not access the redirected file.
- Pilot Scale Testing Report — Google Drive file ID `1zj2W3EnpDle4CWewX9QPhnBfP5VAwEgR`; web page only exposed a Google Drive sign-in/loading screen, so file bytes/content not retrieved.
- Supplementary Phase II Study — official project-site link surfaced, but PDF fetch failed.
- Project Description — official project-site link surfaced, but PDF fetch failed.
- Sludge Thickness Determination — Google Drive file ID `1h-mTHes_jBLzMDt57UZEFGE54J7YJorT`; web retrieval returned cache miss.
- Quantitative Human Health and Ecological Risk Assessment, Phase I ESA and Phase II ESA — listed as large Google Drive downloads; not retrieved in this pass.

The RODD itself is particularly important because its executive summary explicitly qualifies the “Qualified Remedial Options”: they are not necessarily final decisions and could change following executive direction, regulator conditions, new assessments, pilot testing, unknowns and environmental assessment outcomes. It should be used as a dated design/options snapshot, not as proof of final approved or completed work.

The Design Requirements Document is a 2017 conceptual requirements source. It defines functional/performance/safety/operational requirements and includes a site layout/study-boundary figure. It says the conceptual design scope included remediation of groundwater as well as soil, sediment and surface water; that scope statement must not be confused with the later federal Decision Statement's specific condition 5.5 media list.

**Preservation status:** all three successfully opened PDFs have been read in browser-rendered form, but no original PDF binary has yet been downloaded into the controlled evidence vault or SHA-256 hashed. They are therefore content-reviewed, not source-file-preserved.


## 14. Additional browser-text review record — Project MUSE oral-history article

| User inventory item | Source identity | Review status | Preservation status | Notes |
|---|---|---|---|---|
| 63 — `pdf` | Castleden et al. (2017), “Put It Near the Indians”: Indigenous Perspectives on Pulp Mill Contaminants in Their Traditional Territories, Project MUSE article 661289, DOI 10.1353/cpr.2017.0004; https://muse.jhu.edu/article/661289/pdf | **B — Full browser-rendered article text reviewed** | **Not A1/A2.** Original PDF bytes have not been downloaded, hashed or preserved in the evidence vault | This is the original research article, pp. 25–33. The companion Community Policy Brief is a separate item, DOI 10.1353/cpr.2017.0003. The article is recorded as BH-113 in Document 05. The user’s local phone copy was not accessed. |

This row records online text review only. It does not assert that the local file was inspected or that the source binary was acquired.


## 15. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|


## 16. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 1 | `Supplementary+Phase+2+Study` | GHD, *Supplemental Phase 2 Environmental Site Assessment*, Report 11, Project 11148275, 14 September 2018; official PDF: https://static1.squarespace.com/static/5fa9ac321d1bf94e1f13e118/t/5fb2fc6aa269ed475ca25ce7/1605565624084/Supplementary%2BPhase%2B2%2BStudy.pdf | **B — Full browser-rendered report reviewed**, including main report, sample-location figures, borehole/well logs, embedded QA/QC/data-verification memo and conceptual site model figures | **Not A1/A2.** Original PDF bytes not downloaded to evidence storage, hashed or preserved | Source recorded as BH-115 in Document 05. Important unresolved items: vertical elevations for seven new wells were not surveyed, so no hydraulic gradients could be calculated; Northumberland Strait near-estuary PHC exceedances remained horizontally undelineated; deeper FSP2/FSP3 sediment delineation remained incomplete; confirmation sampling was recommended at BHSL-MW-6 and EST-MW-2. Appendix D (laboratory certificates) is explicitly marked “to be provided with final” and is absent from this copy. The user’s local phone copy was not accessed. |


## 17. User's 71-file inventory — identified source files blocked from online text retrieval

The following files are linked from the official Boat Harbour Remediation Project resources page (https://boatharbourproject.buildns.ca/resources). Their identity is confirmed by the official resource listing and the link targets, but the Google Drive viewer returned only a sign-in/loading page to the current retrieval browser. Attempts to open the Drive viewer and direct-download endpoint did not return document content. These are **not reviewed** and must not be represented as read.

| Inventory item | User-supplied filename | Official resource identity / locator | Status | Required next action |
|---|---|---|---|---|
| 2 | `Sludge_Thicknes...ping_Final_Rpt (1)` | *Sludge Thickness Determination* / Google Drive file ID `1h-mTHes_jBLzMDt57UZEFGE54J7YJorT`; official resources page link 14 | **A0 + E + C** — original final report located but Google Drive retrieval blocked; consultant conference summaries reviewed (BH-171, BH-193, BH-194), not the original report | WSP's 2022 RemTech East presentation (BH-193) separates Boat Harbour fieldwork (Oct–Dec 2019) from ASB fieldwork (Sep–Oct 2021), describes LIF/EC profiling calibrated with cores and bathymetry, and reports >600 profiles and >60 core samples. Slide 30 reports 271,000 m³ competent sludge and 400,500 m³ including transition zone, but the extracted slide text labels both Boat Harbour and ASB and does not unambiguously show whether those volumes are combined or separate. SCG's 2021 abstract (BH-194) reports 504 profiles in the 2019 Boat Harbour program, 50 duplicate stations and 70 duplicate profiles; the 2022 abstract reports >600 profiles across 2019 and 2021 programs. These summaries are not a substitute for the original report or raw data. Obtain the final report, maps, survey database, coordinates, raw LIF/EC profiles, calibration, core logs, volume surfaces, uncertainty analysis and calculation workbook. Do not mark the user's original file as read |
| 3 | `Pilot Scale Testing Report` | GHD, *Pilot Scale Testing Construction Report*, 23 December 2019, approximately 580 pages; Google Drive file ID `1zj2W3EnpDle4CWewX9QPhnBfP5VAwEgR`; official resources page link 11 | **A0 + E + C** — original located but Google Drive retrieval blocked; only secondary/related review material examined (BGC ETR BH-012, consolidated IR responses BH-045, EIS Volumes II/III and 2025 EA report) | Related records report dry dredging difficulty distinguishing sludge from underlying BHSL sediment, lower-than-expected Geotube volume reduction, possible geotextile blinding, capacity and construction/slope-stability uncertainty, and inconsistencies in pilot effluent sample counts/results. BH-045 describes daily grab sampling and 11 weekly composite effluent samples, but this is the proponent's response, not independent verification. BGC's review treated the pilot report as an extra-scope document and did not conduct a detailed data-quality review. Obtain the complete original report, appendices, raw survey/dredge records, geotube fill/settlement data, all lab certificates/EDDs, QA/QC, chain-of-custody and treatment-plant operating logs. Do not mark the user's original file as read |
| 4 | `Phase 2 ESA` | GHD, *Phase 2 Environmental Site Assessment*, Report No. 6, 6 June 2018; Google Drive file ID `13GF_P-VqzDvDWQPTmHtGLC8dPg_TxAWt`; official resources page link 10 | **A0 + E + C** — original report located but Google Drive retrieval blocked; its scope and results are referenced in the Supplemental Phase 2 ESA (BH-115), EIS Volume II and related technical reviews | Related sources indicate that the September 2018 Supplemental Phase 2 ESA was commissioned to address data gaps and further delineate impacts identified in the June 2018 Phase 2 ESA. The original Phase 2 report itself remains unread. Obtain the full report, all figures, appendices, lab certificates, data-verification memo, well/borehole logs and raw sample data; compare every recommendation and unresolved APEC with the supplemental report. Do not treat the supplement as a substitute for the original |
| 5 | `Phase I ESA` | *Phase I ESA.pdf* / Google Drive file ID `1narWx0xmVKWzc9PV6HiOv8iwAgsv14eF`; official resources page link 9 | **A0 + E** — source located; browser retrieval blocked (Drive returned loading/sign-in page). No text reviewed and no binary acquired | Obtain original GHD Report No. 3 (26 October 2017), including historical records review, site reconnaissance, APEC rationale, maps, photographs and limitations |

**Important:** BH-115 (the Supplemental Phase 2 ESA) explicitly says it is to be read with the original June 2018 Phase 2 ESA. It does not replace that report. The original Phase 2 ESA remains a separate, unread inventory item. Similarly, the Pilot Scale Testing Construction Report is a separate technical source, not a substitute for the 2018 Laboratory Treatability Study (BH-114).


## 18. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|


## 19. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|


## 20. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|


## 21. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|


## 22. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 17 | `137892E` | IAAC EIS Appendix U, *Air Quality and Odour Assessment Documentation*; https://iaac-aeic.gc.ca/050/documents/p80164/137892E.pdf | **B — Full browser-rendered Appendix U text reviewed**, including WSP 2018 baseline review, GHD 2020 AERMOD report, emission spreadsheets, background data, criteria, receptor maps and model output tables | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source recorded as BH-120 in Document 05. Modelled TSP/PM10/iron exceedances are not measured conditions; Scenario 7 assumes over 100 trucks/day and twice-daily watering for 80% dust control. Modelled H2S odour exceedance occurs in an uninhabited off-site area; sensitive-receptor result is below the 13 µg/m³ odour criterion. Baseline data uses Jan–Sep 2020 after mill closure and pilot work; raw Stantec records, lab certificates, model files and native emission spreadsheets remain outstanding. The 2025 EA reports that speciated sulphur non-detections had detection limits above criteria, and Health Canada identified waste-hauling trucks omitted from the model. The user’s local phone copy was not accessed. |


## 23. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 21 | `137888E` | IAAC EIS Appendix Q, Nova Scotia Lands/GHD, *PLFN Open House No. 1 Summary Report* (27 August 2019); https://iaac-aeic.gc.ca/050/documents/p80164/137888E.pdf | **B — Full browser-rendered report reviewed**, including Appendices A–D | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source recorded as BH-121 in Document 05. 31 attendees; proponent-prepared summary of written comments and staff-noted verbal comments, not a transcript or representative survey. Recorded comments show strong opposition among those who commented to keeping waste in the on-site cell and concerns about long-term integrity, trust, health/cultural recovery and whether PLFN concerns were heard. Proponent responses and cost/schedule claims are not independently verified facts. Keep separate from Appendix R / Open House No. 2 (inventory item 20). The user’s local phone copy was not accessed. |


## 24. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 20 | `137889E` | IAAC EIS Appendix R, Nova Scotia Lands/GHD, *PLFN Open House No. 2 Summary Report* (9 December 2019); https://iaac-aeic.gc.ca/050/documents/p80164/137889E.pdf | **B — Full browser-rendered report reviewed**, including Appendices A–C | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source recorded as BH-122 in Document 05. 23 attendees; proponent-prepared summary, not a transcript or representative survey. Continued concern over the on-site cell and consultation; liaison coordinator gathered feedback on temporary bridge/detour and pipeline treatment options, but this summary does not provide a vote/tally or decision record for those choices. Proponent cost/schedule and safety claims are not independent facts. Keep separate from Appendix Q / Open House No. 1 (inventory item 21). The user’s local phone copy was not accessed. |


## 25. User's 71-file inventory — additional reviewed item with explicit data-use restriction

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 19 | `137890E` | Pictou Landing First Nation, *Well-Being Baseline Study*, December 2019, IAAC EIS Appendix S; https://iaac-aeic.gc.ca/050/documents/p80164/137890E.pdf | **B — Full browser-rendered Appendix S reviewed** for methodology, governance and scope | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Existing source entry BH-071 updated. **Critical restriction:** the report states it was prepared solely for PLFN and Nova Scotia Lands for the Boat Harbour EIS and that use of the data beyond that purpose is not permitted. Do not use detailed participant findings, quotes, percentages or underlying data in documentary work without written authorization from PLFN/data custodians. The report is a community-led, mixed-methods well-being baseline, not a pollutant-specific clinical causation study. The user’s local phone copy was not accessed. |


## 26. User's 71-file inventory — additional reviewed item with cultural-data safeguards

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 18 | `137891E` | Membertou Geomatics Solutions, *Mi’kmaq of Nova Scotia Ecological Knowledge Study*, June 2018, IAAC EIS Appendix T; https://iaac-aeic.gc.ca/050/documents/p80164/137891E.pdf | **B — Full browser-rendered report reviewed**, including methods, limitations, traditional-use analysis and appendices | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Existing source entry BH-072 updated. 44 knowledge holders were interviewed from PLFN and Paq’tnkek; field visit lasted five days in June 2018; study area extends 5 km from the project-site boundary. The report defines “current use” as within the 10 years before the 2018 study, not current in 2026. It expressly says the MEKS is not consultation and does not fulfill Crown duty to consult. It acknowledges some traditional activity users were not interviewed. Detailed traditional-use maps and cultural knowledge are not reproduced; obtain PLFN and knowledge-holder authorization before any documentary use or disclosure. The user’s local phone copy was not accessed. |


## 27. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 22 | `137887E` | IAAC EIS Appendix P, Stantec, *Independent Ambient Air Monitoring Program Presentation*, Boat Harbour Remediation Project; https://iaac-aeic.gc.ca/050/documents/p80164/137887E.pdf | **B — Browser-rendered 29-slide PDF text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source recorded as BH-123 in Document 05. Presentation reports 957 samples for 188 contaminants (Aug 2018–Aug 2019), including 22 BaP exceedances among 100 BaP samples; Stantec says no correlation with pilot activities. Real-time PM/H2S exceedances were sub-minute fence-line action-level spot checks, not long-term ambient exceedances. Underlying monthly/daily reports, raw data, lab certificates and QA/QC are not included in this presentation and remain necessary for independent verification. The user’s local phone copy was not accessed. |


## 28. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 23 | `137885E` | IAAC EIS Appendix O, Nova Scotia Lands/GHD, *Boat Harbour Remedial Action Plan Presentation*, 12 March 2019; https://iaac-aeic.gc.ca/050/documents/p80164/137885E.pdf | **B — Full 24-page browser-rendered presentation reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source recorded as BH-124 in Document 05. Presentation says pilot testing and RAP were 80% complete and quantities still required verification. The displayed in-place sediment volume total is arithmetically inconsistent: row values sum to 1,224,000 m³, while displayed total says 1,244,000 m³. Separate waste table uses 1,224,000 m³. Treat all volumes as preliminary until verified against original calculation workbooks and later sludge-thickness mapping. |


## 29. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 24 | `137884E` | IAAC EIS Appendix N, *A’se’k News — Project Update*, containing June 2019 and October 2019 newsletters; https://iaac-aeic.gc.ca/050/documents/p80164/137884E.pdf | **B — Full browser-rendered appendix text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source recorded as BH-125 in Document 05. Contemporaneous updates report pilot dredging changes, a drained-cove dry-dredging test, increased air-monitoring frequency, sludge-thickness mapping, fish survey and well-being survey. October newsletter reports a potential burial-site concern near the pipeline shoreline; the precise location is not reproduced. Newsletter statements are not substitutes for underlying technical reports. |


## 30. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 25 | `137883E` | IAAC EIS Appendix M, GHD, *Boat Harbour Environmental Advisory Committee Meeting Action Items during the EIA*; https://iaac-aeic.gc.ca/050/documents/p80164/137883E.pdf | **B — Full browser-rendered 310-line appendix reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source recorded as BH-126 in Document 05. Action-item records run March 2019–January 2020. Pilot field testing marked wrapped up by July 2019, but reporting remained in progress through January 2020. Air monitoring and EIS work remained ongoing. GPR survey was complete but pipeline decision was still pending on 15 January 2020. These are status summaries, not full minutes or proof of final completion/acceptance. |


## 31. User's 71-file inventory — source located, full-text retrieval blocked

| Inventory item | User-supplied filename | Official source identity / locator | Status | Required next action |
|---|---|---|---|---|
| 26 | `137882E` | IAAC EIS Appendix L, *Minutes from BHCC Meetings During EIA and Meeting with PLFN to Review Draft EIS*; https://iaac-aeic.gc.ca/050/documents/p80164/137882E.pdf | **B — Full 1,432-line browser-rendered appendix reviewed**, including February 22, May 31, August 27, October 8 and December 4, 2019 BHCC records, February 21, 2020 PLFN draft-EIS review minutes and attached presentation/email | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-179. February 2019 minutes record PLFN concern about on-site containment and a federal EA; pilot dredging was removing too much clean underlying harbour bottom, potentially increasing waste volume/costs. May 2019 action items include an independent qualified firm to review the HHERA when complete. October/December 2019 records show HHERA still in progress, a draft sent to PLFN counsel, pilot debrief rescheduling and unresolved land-transfer/borrow-source items. The Feb 21 2020 meeting records PLFN decisions reflected in the EIS: sidewalks on both bridge sides, a bridge bypass, and removal of pipeline from Indian Cross Point to Highway 348. It also records Chief Andrea Paul's concern that community members did not fully understand the containment cell and her request for a neutral, factual explainer video covering options, design, leachate management and post-closure effects. The proponent's minutes state that the monitoring section is only a framework; details were to be developed with individual approvals after EA approval. An attached Feb 21 email quotes OIC 96-621 and records NS Lands' interpretation that the containment cell is not included in the land-transfer authorization. This is NS Lands' interpretation, not a legal ruling. The GHD minutes state they are GHD's record of the meeting and assume accuracy unless corrected in writing within five days. |


## 32. User's 71-file inventory — partial text review

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 27 | `137881E` | IAAC EIS Appendix K, *Correspondence with the Assembly of Nova Scotia Mi’kmaq Chiefs, PLFN, and the Native Council of Nova Scotia*; https://iaac-aeic.gc.ca/050/documents/p80164/137881E.pdf | **B — All 17 pages / 117-line browser-rendered text extraction reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-127 updated. Assembly resolution (25 April 2019) authorized PLFN to lead consultation on the project on behalf of the Assembly; the July 2 letter recognizes Chief Andrea Paul as PLFN signatory for participant-funding documents. March 9, 2020 NCNS meeting summary records concerns about air quality, archaeological resources, birds, mammals, fish, wetlands, possible contamination reaching the Strait, containment-cell long-term monitoring/liability, hydrology/hydrogeology and pipeline removal. It says NCNS was generally supportive of PLFN's choices but questioned why the entire on-land pipeline would not be removed; this is the proponent's meeting summary, not an NCNS endorsement. NCNS asked whether an outside entity could take on long-term monitoring/maintenance; NS Lands said yes. The summary's “complete characterization” statement is a proponent assertion, not proof that sampling coverage was complete. The PDF includes the Project Description executive-summary attachment, but this review did not separately audit that document's full contents. |


## 33. User's 71-file inventory — partial text review

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 28 | `137880E` | IAAC EIS Appendix J, *Documentation of Formal PLFN Consultation Prior to Determination of Requirement for Federal Environmental Assessment*; https://iaac-aeic.gc.ca/050/documents/p80164/137880E.pdf | **C — Full 641-line browser-rendered text extraction reviewed; correspondence exhibits remain unread** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-128 updated. Extracted content includes the 18 April 2018 consultation-initiation letters to 13 Indigenous communities and the 19 April remedial-options presentation. Matrix weights: regulatory 14%, technical 26%, environmental 24%, social 14%, economic 22%. It ranks on-site disposal above off-site, pipeline abandonment above fill/removal, and ex-situ wetland remediation above natural attenuation. The PLFN counsel letter and Province's 23 August 2018 response are listed but absent from the text extraction; the Province's 2024 IR82 package (BH-180) later quotes PLFN's strong opposition to leaving contamination at or near Boat Harbour and its willingness to wait for another containment facility. Do not treat the matrix as PLFN consent. A 20,000 m³ inconsistency exists between the presentation's reported in-place total and its component rows. |


## 34. User's 71-file inventory — partial review; large bundled appendix

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 29 | `137879E` | IAAC EIS Appendix I, *Documentation of Informal PLFN Consultation*; https://iaac-aeic.gc.ca/050/documents/p80164/137879E.pdf | **C — Text-readable sections of the 5,874-line browser-rendered PDF reviewed; the full 39 MB bundle is not fully reviewed.** The 2014 AIP, Steering Committee ToR, funding MOA, burial-ground agreement, introduced 2015 Bill, 2015 focus-group/Q&A, 2016–2018 BHCC action-item records, 2018 containment-cell options presentation and opening sections of the 2019 Land Use Plan were reviewed. Later embedded records and image-only pages remain incomplete | **Not A1/A2.** Original 39 MB PDF bytes not downloaded, hashed or preserved | Source BH-129 updated; primary subdocuments indexed separately as BH-181–BH-184. The 16 June 2014 AIP requires the Province and PLFN to negotiate in good faith and execute a separate agreement respecting closure/remediation, with terms including closure timelines, PLFN participation costs and Indian Cross Point burial-site protection. The 14 October 2014 funding MOA says it satisfies only AIP clause 2(b); the burial-ground agreement says it is meaningful progress but does not fulfill all clause 2(c). The reproduced 2015 Bill is marked “as introduced” and defines the Facility as the treatment system and pipeline. The May 2015 government Q&A promised extensive cleanup sampling, public release of all results, an independent monitor/program for the life of the project, continuous air/water monitoring and a detailed EMP before work; these are historical commitments, not proof of delivery. The 2018 options presentation records PLFN Chief and Council strongly opposing contamination left at/near Boat Harbour, while also discussing possible PLFN capacity to monitor/manage the cell; this is not evidence of consent to the cell. BHCC action items repeatedly assign NS Lands to prepare independent-monitoring scenarios for PLFN from 2016 through 2018; the visible entries do not show completion. The 2019 Land Use Plan assumes pending land transfers and waters will be deemed safe and says no water-source-protection-zone plan had been found for the PLFN wellfield near the Strait outlet. The plan is marked Final (6 Feb 2019), but related EIS text says adoption was pending. Sensitive burial-ground maps/coordinates and private details are not reproduced. The later subdocuments (Commercial Regional Results, Community Session 2 posters, By-law No.1, Indigenous Opportunities report, Project Charter and other meeting/training materials) remain to be reviewed. |


## 35. User's 71-file inventory — partial review; scanned correspondence not readable

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 30 | `137878E` | IAAC EIS Appendix H, GHD, *Public Correspondence — Project Overview Sent to Local Organizations*; https://iaac-aeic.gc.ca/050/documents/p80164/137878E.pdf | **C — Browser text extraction of the 22-page PDF reviewed; overview and one 2019 email readable** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-130 updated. The April 2017 overview promises that all cleanup samples/results will be public, says Little Harbour and Chance Harbour are being studied as analogues for the former “clean” condition, and forecasts about four years of cleanup after the planned January 2020 closure. Pages 4–20 contain 17 scanned Open House No. 1 comment sheets that remain unread; do not claim public comments have been analyzed. The final 2019 email requests the final report and student thesis from a 2018 Moodie Cove study, plus Lighthouse Beach ownership information and full open-house slides. |


## 36. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 31 | `137877E` | IAAC EIS Appendix G, GHD, *Agency Meeting Minutes*; https://iaac-aeic.gc.ca/050/documents/p80164/137877E.pdf | **B — Full browser-rendered 1,701-line appendix reviewed**, including June/September/November/December 2019 meetings and February 2020 agency sessions/presentation | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source recorded as BH-131 in Document 05. Health Canada identified potentially under-conservative HHERA assumptions (4-day exposure averaging and omission of hand-to-mouth sediment ingestion at the water's edge); the meeting record says the scenario was revised to 8 h/day, 7 days/week, 30 weeks/year for a toddler on mudflats. Verify this in final HHERA Appendix A. June 2019 minutes said no additional marine baseline data were anticipated; later 2025 regulator review identified marine/sensitive-habitat and sediment-transport gaps. December 2019 minutes report some PLFN participants still opposed or did not understand the cell; they record a community voting mechanism but no vote tally/result. Meeting records are GHD interpretations, not transcripts. |


## 37. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 32 | `137876E` | IAAC EIS Appendix F, GHD/Nova Scotia Lands, *Public Open House No. 2 Documentation — Display Panels and Summary Report* (10 December 2019); https://iaac-aeic.gc.ca/050/documents/p80164/137876E.pdf | **B — Full 23-page browser-rendered PDF text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source recorded as BH-132 in Document 05. The public-session summary says tidal-transport modelling was still outstanding, estimated project cost at about $250 million, and forecast a late-2021 start with 4–7 years of remediation. It contains proponent statements of no groundwater contamination and no pilot-related air increases/odours; reconcile with the 2018 Supplemental Phase 2 ESA and Stantec monitoring presentation before repeating. Distinct from the PLFN-only Open House No. 2 summary (Appendix R / item 20). |


## 38. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 33 | `137874E` | IAAC EIS Appendix D, GHD/Nova Scotia Lands, *Boat Harbour Environmental Advisory Committee Terms of Reference*, 22 January 2016; https://iaac-aeic.gc.ca/050/documents/p80164/137874E.pdf | **B — Full browser-rendered 81-line text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source recorded as BH-133 in Document 05. The ToR is explicitly a **draft for discussion**, not proof of an approved committee charter. It makes BHEAC advisory to Nova Scotia Lands; NS Lands appoints the chair and retains project decision authority; BHEAC is not a regulator or independent monitor. Obtain the approved ToR and full recommendation/response records before describing how the committee operated. |


## 39. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|


## 40. User's 71-file inventory — source located, full-text retrieval blocked

| Inventory item | User-supplied filename | Official source identity / locator | Status | Required next action |
|---|---|---|---|---|


## 39. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 34 | `137875E` | IAAC EIS Appendix E, GHD/Nova Scotia Lands, *Public Open House No. 1 Documentation* (1 August 2019); https://iaac-aeic.gc.ca/050/documents/p80164/137875E.pdf | **B — Full 53-page browser-rendered PDF text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source recorded as BH-134 in Document 05. Proponent's 2019 display panels say no contaminated sediment had been found beyond the estuary or in the Northumberland Strait; treat as a survey-bounded proponent statement, not proof of absence. Later 2025 DFO/IAAC concerns about model extent and missing sensitive-habitat data require reconciliation. The public comment summary lists 17 written comments (six positive), not a representative measure of community opinion. |


## 40. User's 71-file inventory — three official appendices identified but not retrieved

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 35 | `137873E` | IAAC EIS Appendix C, *Public Meeting Minutes*; official registry index lists 401 KB; https://iaac-aeic.gc.ca/050/evaluations/proj/80164/document/137959 | **E — retrieval blocked.** Registry title/identity verified; direct PDF and registry-link fetch both timed out | **Not A1/A2.** No binary downloaded or hashed | Source BH-135. Exact meeting dates, participants, minutes, decisions and action items remain unknown. Do not substitute other appendices' minutes. |
| 36 | `137872E` | IAAC EIS Appendix B, *Environmental Management and Control Documents*; official registry index lists 17 MB; https://iaac-aeic.gc.ca/050/evaluations/proj/80164/document/137959 | **E — retrieval blocked.** Registry title/identity verified; direct PDF and registry-link fetch both timed out | **Not A1/A2.** No binary downloaded or hashed | Source BH-136. Underlying management plans/control documents remain unread; obtain and review each document's revision, scope, thresholds, contingencies and responsible parties. |


## 41. User's 71-file inventory — EIS Volumes I–III identified but not retrieved

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|


## 42. User's 71-file inventory — source located, original 154 MB appendix unread

| Inventory item | User-supplied filename | Official source identity / locator | Status | Required next action |
|---|---|---|---|---|
| 37 | `137871E` | IAAC EIS Appendix A, GHD / Nova Scotia Lands, *Human Health and Ecological Risk Assessment* (154 MB), official registry attachment: https://iaac-aeic.gc.ca/050/documents/p80164/137871E.pdf; registry index: https://iaac-aeic.gc.ca/050/evaluations/proj/80164/document/137959 | **A0 + E + C** — source identity confirmed; direct fetch and registry link timed out. Original HHERA has not been read. Related 2022 Health Canada information requests and the 2025 IAAC EA report were reviewed as secondary/regulatory context only; they are not substitutes for Appendix A | Obtain the 154 MB original as smaller sections or from the proponent/IAAC, including all appendices, exposure calculations, sample data and lab certificates. Independently audit the conceptual site model, operable exposure pathways, country-food species/tissues, background surrogates, toxicity reference values, exposure frequency/duration, SSTL calculations, soil allocation factors, uncertainty/sensitivity analysis and risk characterization. Reconcile the November 2019 Health Canada meeting record's toddler sediment exposure assumptions (8 h/day, 7 days/week, 30 weeks/year) with the 2025 EA report's footnote describing 4 h/day, 7 days/week. Address Health Canada's 2022 concerns about vanadium and dioxin/furan soil allocation factors, repeated sub-chronic exposure, and use of cattails/bulgeweed as background surrogates for other plant species. Do not claim the HHERA itself has been reviewed until the original is obtained |


## 42. User's 71-file inventory — 2025 federal report reviewed; seven historical PDFs identified but not text-reviewed

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 44 | `23.2009BandNewsletter` | Pictou Landing First Nation Chief and Council, *2009 Band Newsletter*; https://signalhfx.ca/wp-content/uploads/2019/02/23.2009BandNewsletter.pdf | **C — Original 3-page PDF remains unread** (no browser text extraction; screenshot cache miss). BH-175 provides the archive description; BH-185's 23 April 2009 investigative article quotes the newsletter as saying PLFN would “fight to protect our collective right to be free from the Boat Harbour treatment facility” and that its position was strong. BH-185 also quotes the 4 December 2008 Minister Murray Scott closure commitment | **Not A1/A2.** No binary downloaded or hashed. The article is not the newsletter and does not verify its full contents, publication date, exact wording or whether the quote is complete. Obtain readable original before quotation or full attribution. |
| 45 | `22.2008AccomodationAgreement` | Northern Pulp, proposed *Accommodation Agreement* (late 2008); https://signalhfx.ca/wp-content/uploads/2019/02/22.2008AccomodationAgreement.pdf | **C — Archive description plus secondary negotiation account.** Original 2-page PDF has no extractable text; screenshot retrieval failed. BH-175 and BH-185 (2009 Signal investigative article) report that Northern Pulp proposed an interim effluent-extension arrangement, sent a $110,000 cheque and PLFN counsel returned it because no agreement had been reached. BH-177, a 2020 sworn provincial deputy-minister affidavit, says PLFN and Northern Pulp entered an Accommodation Agreement on 31 December 2008 and PLFN agreed not to oppose only a temporary licence extension to 31 January 2009 while closure/relocation negotiations continued. The 2009 article may describe a proposed interim extension while the affidavit may refer to a different instrument; the original is needed to resolve this | **Not A1/A2.** Original proposal and clauses remain unread; verify whether the $110,000 cheque and proposal refer to this exact instrument. The archive says PLFN did not accept it. Do not characterize legal terms or execution status without the signed/proposed document and correspondence. |
| 46 | `21.MOUopenletter2002` | PLFN, *2002 MOU Open Letter* (circulated to Band members); https://signalhfx.ca/wp-content/uploads/2019/02/21.MOUopenletter2002.pdf | **C — Archive description plus secondary context.** Original 11-page PDF has no extractable text; screenshot retrieval failed. BH-175 reports the 2001 MOU was ratified in 2002 and describes payment/land-transfer terms. BH-177 confirms in a sworn provincial affidavit that the 2001 PLFN–Kimberly-Clark MOU was approved by referendum in July 2002. BH-176's 2013/2014 PLFN submission says the MOU contemplated the settling basin, emergency spill basin and ASB remaining until 31 December 2030, with a bypass pipeline to allow the larger stabilization lagoon to be cleaned and returned to tidal conditions; it says payments began at $200,000/year and land transfer was conditional on the pipeline. These are party-submission summaries, not verified contract clauses | **Not A1/A2.** Original open letter and underlying 2001 MOU remain unread. These are secondary-reported terms and performance, not verified contract clauses. Obtain signed MOU, schedules, ratification/BCR and meeting records, payment ledger, title transfers, 2006 amendment and any releases/consents. |
| 47 | `20.1996lease_license_agreement` | Province of Nova Scotia, *1996 Lease License Agreement*; https://signalhfx.ca/wp-content/uploads/2019/02/20.1996lease_license_agreement.pdf | **C — Archive description plus secondary context.** Original 8-page PDF has no extractable text; screenshot retrieval failed. BH-174 and BH-175 provide secondary context. BH-177 identifies a 1995 MOU framework that generated separate Water Supply, Lease, Indemnity, Equipment Lease and License agreements, and records OIC 96-621 as ratifying related arrangements; it does not reproduce this 1996 equipment lease/licence | **Not A1/A2.** Parties, assets, term, rent, maintenance, liabilities and relationship to the 1995 instruments remain unverified. Do not infer the 1996 instrument's clauses from the secondary history. |
| 48 | `19.1995indemnity_agreement` | *1995 Indemnity Agreement*; https://signalhfx.ca/wp-content/uploads/2019/02/19.1995indemnity_agreement.pdf | **C — Archive description plus secondary context.** Original 4-page PDF has no extractable text; screenshot retrieval failed. BH-174 and BH-175 report the Province retained responsibility for waste deposited before the 1995 operating arrangement. BH-177 confirms that an Indemnity Agreement was one of the separate instruments contemplated by the 1995 MOU; it does not reproduce the actual indemnity clauses | **Not A1/A2.** Full indemnity wording, covered parties, exclusions, duration, and relationship to the lease/licence remain unreviewed. Do not treat the articles' summaries as the legal clause. |
| 49 | `18.1995lease_agreement` | *1995 Lease Agreement*; https://signalhfx.ca/wp-content/uploads/2019/02/18.1995lease_agreement.pdf | **C — Archive description plus secondary context.** Original 9-page PDF has no extractable text; screenshot retrieval failed. BH-174 and BH-175 describe the Province–mill arrangement. BH-177 identifies the 1995 MOU framework and separate Lease Agreement; the actual lease terms, property schedules and indemnity scope remain unread | **Not A1/A2.** Exact parties, property, term, renewal, termination, liability and operating obligations remain unreviewed. Obtain signed agreement and schedules; do not treat the articles' summaries as contract wording. |
| 50 | `17.1995licenseagreement` | *1995 License Agreement*; https://signalhfx.ca/wp-content/uploads/2019/02/17.1995licenseagreement.pdf | **C — Archive description plus secondary context.** Original 4-page PDF has no extractable text; screenshot retrieval failed. BH-174 and BH-175 report the 1995 operating arrangement. BH-177 identifies a separate License Agreement as one of the 1995 MOU instruments; the original licence and amendments remain unread | **Not A1/A2.** Authorized activities, conditions, compliance duties, term, renewal and termination remain unreviewed. Obtain the signed licence and all amendments; do not treat the articles' summaries as licence wording. |


## 43. User's 71-file inventory — early historical records identified but not text-reviewed

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 51 | `13.1989-statementofdefence` | Government of Canada, *1989 Statement of Defence*; https://signalhfx.ca/wp-content/uploads/2019/02/13.1989-statementofdefence.pdf | **C — Archive description plus secondary excerpt.** Original six-page PDF has no extractable text; screenshot cache miss. The 2009 *Laid to Waste* article (BH-172) identifies the 17 July 1989 filing and summarizes/quotes the federal defence's position that PLFN had agreed to the mill-waste use and that Rust-era improvements had cured the septic/pollution condition | **Not A1/A2.** Original pleading not read or hashed. Obtain court-filed original and compare exact admissions/denials, legal arguments and amendments with the 1986 defence and statement of claim. Attribute the excerpt to the 2009 article until verified against the pleading. |
| 52 | `12.1986defencesmaller` | Government of Canada, *1986 Defence*; https://signalhfx.ca/wp-content/uploads/2019/02/12.1986defencesmaller.pdf | **C — Archive title/description only.** PDF opened as seven pages but no text extraction; screenshot cache miss | **Not A1/A2.** No binary downloaded or hashed | Source BH-148. Original defence not read; do not treat PLFN allegations as admissions by Canada. |
| 53 | `10.1970_letter_from_rowe` | E.L.L. Rowe, *1970 Letter From Rowe*; https://signalhfx.ca/wp-content/uploads/2019/02/10.1970_letter_from_rowe.pdf | **C — Archive description only.** PDF opened as three pages but no text extraction; screenshot cache miss | **Not A1/A2.** No binary downloaded or hashed | Source BH-154. Government response to the church minister's letter; exact contents unreviewed. |
| 54 | `09.1970smithfromchurch` | Rev. D. Glass, Sharon–Saint John United Church, *1970 Church Letter* to Premier G.I. Smith; https://signalhfx.ca/wp-content/uploads/2019/02/09.1970smithfromchurch.pdf | **C — Archive description only.** PDF opened as one page but no text extraction; screenshot cache miss | **Not A1/A2.** No binary downloaded or hashed | Source BH-153. August 1970 protest letter; exact text unreviewed. BH-186 cites the letter as a contemporary source on public opposition, but does not substitute for the original. |
| 55 | `08.chipmanletter` | New Glasgow Lions Club, *Chipman Letter*; https://signalhfx.ca/wp-content/uploads/2019/02/08.chipmanletter.pdf | **C — Archive description only.** PDF opened as three pages but no text extraction; screenshot cache miss | **Not A1/A2.** No binary downloaded or hashed | Source BH-152. Archive says it expresses grave concern; exact author/date/content unreviewed. |
| 56 | `08.1970fergusonrustletter` | Henry Ferguson, *1970 Ferguson-Rust Letter*; https://signalhfx.ca/wp-content/uploads/2019/02/08.1970fergusonrustletter.pdf | **C — Archive description plus secondary quotation only.** PDF opened as four pages but no text extraction; screenshot cache miss | **Not A1/A2.** No binary downloaded or hashed | Source BH-151. BH-186 (Mark Leeming, 2017) quotes a passage on air pollution, pipeline leakage and tidal movement of pollution; verify the quotation against the handwritten original before documentary use. |
| 57 | `07.1970macDonaldLetterComplete` | Dr. Joseph B. MacDonald, *1970 MacDonald Letter* to Rust Consultants; https://signalhfx.ca/wp-content/uploads/2019/02/07.1970macDonaldLetterComplete.pdf | **C — Archive description plus secondary excerpt.** Original eight-page PDF has no extractable text; screenshot cache miss. The 2009 *Laid to Waste* article (BH-172) identifies a 22 March 1970 letter and reports MacDonald's criticism of treatment adequacy, toxicity, low oxygen and failure to install aerators; BH-186 also cites the letter as an archival source | **Not A1/A2.** Original handwritten letter not read or hashed. Verify exact text, author(s), date, addressee and attachments before quoting; observations and technical claims require independent corroboration. |
| 58 | `05.1966orderincouncil` | Government of Canada, *1966 Order in Council* concerning Boat Harbour riparian rights; https://signalhfx.ca/wp-content/uploads/2019/02/05.1966orderincouncil.pdf | **C — Archive description plus secondary historical/legal context.** Original two-page OIC has no extractable text; screenshot cache miss. The 2009 *Pulp mill’s warm welcome* article (BH-173) says the 2 September 1966 OIC confirmed the arrangement but did not grant Nova Scotia the absolute control it wanted. PLFN's 2013/2014 legal submission (BH-176) argues that riparian rights could not be transferred without a valid Indian Act surrender or transfer-in-lieu-of-expropriation process and says no qualifying meeting/referendum or provincial expropriation enactment existed; it also identifies the OIC's conditions as remedial action if Boat Harbour became septic, construction of a slipway and $60,000 compensation. The 2010 PLFN Statement of Claim (BH-178) advances the same legal position. The PLFN MEKS (BH-072) describes the transfer as purported | **Not A1/A2.** Original OIC not read or hashed. Obtain certified OIC, BCR, Indian Affairs file and maps/schedules. The legal effect is unresolved; do not state that the rights were validly transferred or that the OIC was legally ineffective without full legal analysis. |
| 59 | `04.1966ProposedTreatment` | Conlon Engineering, *1966 Proposed Treatment Estimate*; https://drive.google.com/file/d/1WdGIw7W2u0gMGn9eiAeOTHUG0zWXQkU1/view | **C — Archive description only.** Google Drive link returned a sign-in page; underlying file not read | **Not A1/A2.** No binary downloaded or hashed | Source BH-158. Archive describes estimate up to approximately $100,000; scope and cost basis unverified. |
| 60 | `03.1966Macdonaldhammletter` | Dr. Joseph B. MacDonald / Dr. Hamm, *1966 MacDonald-Hamm Letter*; https://signalhfx.ca/wp-content/uploads/2019/02/03.1966Macdonaldhammletter.pdf | **C — Archive description plus secondary excerpt.** Original two-page PDF has no extractable text; screenshot cache miss. The 2009 *Pulp mill’s warm welcome* article (BH-173) identifies a 19 March 1966 letter from Dr. Joseph B. MacDonald to Premier Robert Stanfield and summarizes its criticism of the proposal; the MEKS (BH-072) cites the letter as MacDonald & Hamm (1966) | **Not A1/A2.** Original letter not read or hashed. Authorship and addressee remain unresolved because the filename/title says “MacDonald-Hamm”/“to Hamm,” while the article identifies MacDonald writing to Stanfield. Verify the original signature, addressee and full text before attribution or quotation. |
| 61 | `02.1966Reportfo...eexecutivecouncil` | Nova Scotia Water Authority / responsible Minister, *1966 Water Act Report*; https://signalhfx.ca/wp-content/uploads/2019/02/02.1966Reportfortheexecutivecouncil.pdf | **C — Archive description only.** PDF opened as one page but no text extraction; screenshot cache miss | **Not A1/A2.** No binary downloaded or hashed | Source BH-156. Archive says it recommends authorization to turn Boat Harbour into an industrial waste lagoon; exact recommendation and conditions unreviewed. |
| 62 | `01.1965executive...ncil_province_mill` | Province of Nova Scotia, *1965 Order in Council*; https://signalhfx.ca/wp-content/uploads/2019/02/01.1965executivecouncil_province_mill.pdf | **C — Archive description only.** PDF opened as three pages but no text extraction; screenshot cache miss | **Not A1/A2.** No binary downloaded or hashed | Source BH-155. Archive says it authorized a plan to dam the Middle River branch for a mill water-supply reservoir; exact authority, conditions and scope unreviewed. |


## 43. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 40 | `137221E` | GHD / Nova Scotia Lands, *Environmental Impact Statement, Volume III of V*; https://iaac-aeic.gc.ca/050/documents/p80164/137221E.pdf | **B — Browser-rendered text reviewed; Sections 4–6 (public/agency engagement, Mi’kmaq consultation and rights/accommodation analysis) examined** | **Not A1/A2.** Original 9 MB PDF bytes not downloaded, hashed or preserved | Existing source entry BH-138 updated. The EIS records PLFN's May 2018 position as strongly opposed to permanent on-site containment and prepared to wait for an off-site option; individual comments show varied views, so do not call the position unanimous. It records a January 2020 PLFN decision to remove the pipeline between Indian Cross Point and Highway 348. It acknowledges long-term waste storage in the cell restricts access/use and is an adverse rights impact. It lists 128 ha to be offered after remediation and 45.2 ha of further contemplated transfers, conditional on remediation and acceptable standards that PLFN was still developing. The EIS's “net positive” rights conclusion is the proponent's analysis, not a community finding. Avoid parcel identifiers and sensitive burial-site details. |


## 44. User's 71-file inventory — additional full-text reviews and duplicate identification

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 43 | `En106-278-2025-eng` | IAAC, *Boat Harbour Remediation Project — Environmental Assessment Report*, January 2025; Government of Canada Publications PDF https://publications.gc.ca/collections/collection_2025/aeic-iaac/En106-278-2025-eng.pdf | **B — Full browser-rendered report reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Existing source BH-009. This is the same publication as inventory item 65 (`160559E`): matching title, catalogue number En106-278/2025E-PDF and ISBN 978-0-660-74686-9. Treat as one report, not independent corroboration. |
| 65 | `160559E` | IAAC registry copy of the January 2025 *Environmental Assessment Report*; https://iaac-aeic.gc.ca/050/documents/p80164/160559E.pdf | **B — Full browser-rendered 156-page report reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Duplicate/alternate registry copy of inventory item 43, same publication title, catalogue number and ISBN. Cross-reference BH-009; do not count as a separate study or independent evidence. |
| 66 | `Design+Requirements+Document` | GHD for Nova Scotia Lands, *Design Requirements Document*, Report No. 4, 12 September 2017; https://boatharbourproject.buildns.ca/s/Design-Requirements-Document.pdf | **B — Full browser-rendered 37-page text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-160. Conceptual design-basis document, not final design. Key discrepancy: 2017 post-dewatering estimate ~230,000 m³ versus 2018 RODD final-disposal estimate 517,700 m³. Long-term ecological restoration/maintenance explicitly outside this design scope; 2:1 wetland replacement is a requirement, not proof of delivery. |
| 67 | `Remedial+Option...ent_compressed` | GHD for Nova Scotia Lands, *Remedial Option Decision Document*, Report No. 5, 1 May 2018; https://boatharbourproject.buildns.ca/s/Remedial-Options-Decision-Document_compressed.pdf | **B — Full browser-rendered 406-page combined document reviewed**, including embedded Laboratory Treatability Study and appendices | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-161. Qualified options included vertical expansion of existing cell, ex-situ wetland remediation, clean/inspect/abandon pipelines, hydraulic dredging/geotubes, low-tech treatment of bulk/dewatering water and off-site leachate disposal. The report itself says options were qualified recommendations, not necessarily final decisions, and could change after pilot testing, EA, regulator direction and new information. Waste figures: 1,224,000 m³ in place; 517,700 m³ final disposal assuming dewatering. Class D 2018-dollar costs are estimates, not actual expenditure. |


## 45. User's 71-file inventory — remaining status reconciliation

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 11 | `137898E` | IAAC EIS Appendix AA, *Riparian, Wetland and Terrestrial Environments Assessment Documentation*; official index https://iaac-aeic.gc.ca/050/evaluations/proj/80164/document/137959 | **E — identified, direct retrieval timed out**. Official registry index lists 42 MB | **Not A1/A2.** No binary downloaded or hashed | Source BH-166. Full appendix unread; wetland delineation, vegetation/terrestrial habitat survey methods, raw data, field sheets and GIS remain required. |
| 63 | `pdf` | Castleden et al. (2017), “Put It Near the Indians”: Indigenous Perspectives on Pulp Mill Contaminants in Their Traditional Territories, Project MUSE article 661289, DOI 10.1353/cpr.2017.0004; https://muse.jhu.edu/article/661289/pdf | **B — Full browser-rendered PDF text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-113. This is the peer-reviewed original research article (pp. 25–33), distinct from its companion Community Policy Brief (DOI 10.1353/cpr.2017.0003, pp. 23–24) and distinct from Bennett's 2013 thesis (item 64). Ten Elders participated in community-based oral-history research. Oral histories/lived experience must not be represented as pollutant-specific epidemiological causation. |
| 64 | `Bennett-Ella-ME...RES-August-2013` | Ella Bennett, *“We Had Something Good and Sacred Here”: ReStorying A’se’k with Pictou Landing First Nation*, Dalhousie University Master’s thesis, 2013 | **B — Full browser-rendered thesis text reviewed** | **Not A1/A2.** Original thesis bytes not downloaded, hashed or preserved | Source BH-164. Separate thesis that informs the 2017 Project MUSE article; do not merge the two works. Apply participant/PLFN permissions and cultural-data safeguards to oral histories and sensitive knowledge. |
| 68 | `2025-Annual-Report-to-IAAC-Final` | Build Nova Scotia, *Boat Harbour Remediation Project 2025 Annual Report*, March 2026; https://buildns.ca/wp-content/uploads/2026/03/2025-Annual-Report-to-IAAC-Final.pdf | **B — Full browser-rendered 25-page report reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-011. Report covers 24 Jan–31 Dec 2025. Proponent says project remained pre-construction; no substantive project planning or follow-up monitoring was undertaken. Indigenous monitors and independent environmental monitor not yet retained. Alternative Site Advisory Committee formed, ToR executed, first alternative site selected; separate Condition 9 report submitted 22 Jan 2026. Do not infer 2026 court or project status from this 2025 reporting period. |
| 69 | `Nova-Scotia-Lan...der-June-01-2021` | Nova Scotia Environment and Climate Change, Ministerial Order MO-60007 to Nova Scotia Lands Inc., issued 28 May 2021; https://novascotia.ca/nse/issues/docs/Nova-Scotia-Lands-Ministerial-Order-June-01-2021.pdf | **B — Full browser-rendered 25-page order reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-101. Effective monitoring date 1 June 2021. Requires quarterly groundwater/surface-water monitoring, air monitoring/quarterly QA/QC reports, well inspections, immediate reporting of groundwater-quality changes, annual water reports with lab certificates and groundwater gradients/flow direction, 15-year records and site TSS discharge limits. Appendix B uses BHETF monitoring wells; not PLFN production wells. |
| 70 | `MO-60003-NPNSC` | Nova Scotia Environment and Climate Change, Ministerial Order MO-60003 to Northern Pulp, 14 May 2020; https://novascotia.ca/nse/issues/docs/MO-60003-NPNSC.pdf | **B — Full browser-rendered order text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-163. Requires transition management/aeration, Point C/D monitoring, collection/treatment of impacted stormwater and leachate, pipeline decommissioning plan, TRS monitoring and quarterly QA/QC, groundwater/surface-water sampling, 15-year well records and annual reports with certificates and trends. Revoked 5 July 2021. |
| 71 | `55774-Ministerial...S-January-2020` | Nova Scotia Environment and Climate Change, Ministerial Order MO-55774 to Northern Pulp, 29 January 2020; https://novascotia.ca/nse/issues/docs/55774-Ministerial-Order-NPNS-January-2020.pdf | **B — Full browser-rendered order text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-162. Requires pulp production cessation before 31 Jan 2020, wastewater cessation by 30 Apr 2020, pipeline inspection/decommissioning plans, effluent monitoring and ambient TRS/TSP/PM2.5 monitoring at Pictou Landing and Greenhill. Revoked 5 July 2021. The revocation PDF title says “May 14 2020” but its body correctly identifies the 29 Jan 2020 MO-55774; preserve this metadata conflict. |

### Inventory status reconciliation
The 71 inventory entries are represented exactly once in this log (71 rows; no missing or duplicate inventory numbers). Current mutually exclusive status counts:

- **B — substantial browser-text review:** 36 files.
- **C — partial/excerpt/archive-description review only:** 24 files.
- **E — source identified but retrieval failed, with no usable content review:** 4 files.
- **C + E — original retrieval failed, but related excerpts/secondary/regulatory material were reviewed:** 7 files.

These counts describe review status, not acquisition. **No original PDF in the 71-file inventory has A1/A2 status in this workflow:** none has been downloaded as the original binary, SHA-256 hashed and preserved in evidence storage. Therefore this log is a complete status register, not a claim that all 71 original PDFs have been fully read or preserved.


## 44. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 41 | `137220E` | GHD / Nova Scotia Lands, *Environmental Impact Statement, Volume II of V*; https://iaac-aeic.gc.ca/050/documents/p80164/137220E.pdf | **B — Browser-rendered text reviewed; core Sections 2–3 (alternatives and project description) and major tables/design assumptions examined** | **Not A1/A2.** Original 12 MB PDF bytes not downloaded, hashed or preserved | Existing source entry BH-139 updated. Key discrepancies to resolve: 2019 RAP deck total 1.224 million m³ in-place versus EIS 770,000–922,000 m³ total waste; 2018 RODD dewatering effluent 0.7–1.7 million m³ versus EIS estimate 5.2 million m³; 2018 liner concept versus 2020 EIS GCL/FML single-composite description; 17,500 versus 18,200 truckloads. EIS says all waste-management alternatives leave the existing ~180,000 m³ cell in place; off-site disposal only removes new remediation waste. It says current leachate monitoring did not include PHCs, dioxins/furans or cyanide, and that the sediment compliance criteria/sampling methodology were still being developed. It also records the on-land pipeline segment from Indian Cross Point to Highway 348 property line for removal, underwater line abandonment, and other on-land segments abandonment in place. |


## 46. EIS Volumes IV and V — inventory rows omitted in earlier status tables

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|


## 45. User's 71-file inventory — partial table-of-contents review only

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 42 | `137219E` | GHD / Nova Scotia Lands, *Environmental Impact Statement, Volume I of V*; https://iaac-aeic.gc.ca/050/documents/p80164/137219E.pdf | **C — Partial browser-text review.** Table of contents and Table of Concordance are readable; substantive EIS narrative sections are not present in the extracted text | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Existing source entry BH-140 updated. The TOC identifies a Northumberland Strait sub-section extending east of the Confederation Bridge to eastern PEI, a 2004 Pictou Road fish/shellfish table and marine cumulative-effects assessment. The IAAC guideline concordance requires marine water quality and bottom-sediment quality/thickness/grain-size/mobility in the estuary and along the Strait shoreline immediately outside Boat Harbour's mouth. These headings do not prove full-Strait sampling. Obtain the narrative pages and verify exact sampling coverage, sample dates, stations, datasets and follow-up monitoring before drawing conclusions about the Strait-wide baseline. |


## 46. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 38 | `137223E` | GHD / Nova Scotia Lands, *Environmental Impact Statement, Volume V of V*; https://iaac-aeic.gc.ca/050/documents/p80164/137223E.pdf | **B — Browser-rendered text reviewed; Sections 8–9 (effects summary and follow-up/monitoring) and references examined** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Existing source entry BH-106 updated. The EIS's no-significant-effects conclusion is the proponent's assessment. Section 9 says monitoring details remain preliminary and must be finalized with regulators, scientific advisors and PLFN. It proposes independent ambient-air monitoring, existing-network groundwater monitoring with annual reports, wet/dry surface-water sampling, and at minimum TSS/BOD monitoring for water discharged to the Strait. Post-remediation marine monitoring is described for the estuary, with parameters/frequency TBD; no full Strait-wide network is specified. Country-food sampling is deferred to HHERA and limited to remediated sediment areas. Noise/light follow-up is complaint-triggered. |


## 47. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 39 | `137222E` | GHD / Nova Scotia Lands, *Environmental Impact Statement, Volume IV of V*, IAAC registry attachment https://iaac-aeic.gc.ca/050/documents/p80164/137222E.pdf | **B — Full browser-rendered text reviewed** (approximately 9,766 extracted lines), with focused analysis of groundwater, surface-water, marine-baseline and selected effects sections | **Not A1/A2.** Original 50 MB PDF bytes not downloaded, hashed or preserved | Existing source entry BH-038 updated. The EIS describes a broad marine regional study area extending east of Confederation Bridge to eastern PEI, but that is a desktop species-presence review, not field sampling across the Strait. The field site area is the estuary/Pictou Road shoreline plus a 1.2 km pipeline corridor. The EIS reports only one Strait surface-water sample and five Strait sediment samples; three sediment samples exceeded PHC screening guidelines. The 2019 open-house summary's blanket “no contaminated sediment in the Strait” statement therefore requires reconciliation. Ten clam samples at the outfall and additional shellfish samples mostly several kilometres away are not a comprehensive Strait-wide baseline. Volume IV also cites the 2018 GHD Well Field Evaluation; its wellfield interpretations must be checked against AECOM 2016, GHD 2018 originals and raw well data. |


## 49. User's 71-file inventory — source located, 230 MB groundwater bundle not retrieved

| Inventory item | User-supplied filename | Official source identity / locator | Status | Required next action |
|---|---|---|---|---|
| 12 | `137897E` | IAAC EIS Appendix Z, *Groundwater and Surface Water Assessment Documentation* (230 MB); https://iaac-aeic.gc.ca/050/documents/p80164/137897E.pdf | **A0 + E + C** — official source identity confirmed; direct PDF and registry retrieval timed out. The 230 MB bundle itself has not been read or acquired. Related selected material is available in EIS Volume IV and 2022 IAAC information requests; individual groundwater reports are separately identified in Document 17 (BH-089, BH-088, BH-091, BH-095 and related leads) | Obtain Appendix Z as separate original reports/attachments rather than one 230 MB file. Priority originals: AECOM 2016 drilling/hydraulic testing and raw pumping tests; GHD 2018 Well Field Evaluation and capture-zone model; Dillon 2003 Phase II groundwater exploration; Dillon 2011 IR24 groundwater monitoring; GHD 2017 Data Gap Assessment; Dillon 2018/2019 sludge-cell monitoring; GHD Sampling and Analysis of Dredge Spoils. Preserve each binary, maps, well logs, coordinates, raw logger series, lab EDDs/certificates and model files. Do not mark Appendix Z complete based on Volume IV excerpts or the 2022 IR summaries |


## 50. User's 71-file inventory — source located, 91 MB geology/geochemistry appendix unread

| Inventory item | User-supplied filename | Official source identity / locator | Status | Required next action |
|---|---|---|---|---|
| 13 | `137896E` | IAAC EIS Appendix Y, *Geology and Geochemistry Assessment Documentation* (91 MB); https://iaac-aeic.gc.ca/050/documents/p80164/137896E.pdf | **A0 + E + C** — official source identity and size confirmed; direct PDF retrieval timed out. Appendix Y itself has not been read | Obtain the appendix in smaller component reports. Review bedrock/overburden stratigraphy, geochemical characterization, acid-generation/metal-leaching potential, soil/sediment chemistry, borehole logs, sample locations/depths, laboratory methods, QA/QC, lab certificates, maps and native GIS. Cross-reference with Appendix Z groundwater pathways, Appendix AA wetlands and the 2025 EA conditions. Do not infer the content from the EIS summary or from the separate Phase II ESA |


## 51. User's 71-file inventory — previously reviewed technical appendices now status-recorded

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 8 | `137901E` | IAAC EIS Appendix DD, *Socio-Economic Assessment Documentation*; https://iaac-aeic.gc.ca/050/documents/p80164/137901E.pdf | **B — Browser-rendered appendix text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-168. PLFN demographic/economic indicators use 2011 Census data where 2016 PLFN data were unavailable, compared against 2016 comparator communities. Fisheries data could not be disaggregated to Band level. Employment and economic benefits are projections, not realized outcomes |
| 9 | `137900E` | IAAC EIS Appendix CC, *Avian Assessment Documentation*; https://iaac-aeic.gc.ca/050/documents/p80164/137900E.pdf | **B — Browser-rendered appendix text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-169. Surveys in 2017–2018 and 2019 identified 40 priority species, including six species at risk. Common Nighthawk survey was a single evening (26 June 2018) at six stations. Later ECCC review identified incomplete northern coverage, uncertainty about Eastern Whip-poor-will targeting, and softwood habitat not represented in transects; verify these issues against the 2022 IR response and any revised surveys |
| 10 | `137899E` | IAAC EIS Appendix BB, *Aquatic Environments Assessment Documentation*; https://iaac-aeic.gc.ca/050/documents/p80164/137899E.pdf | **B — Browser-rendered appendix text reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-170. Includes marine benthic baseline, fish/habitat assessment and bathymetry/LiDAR references. 2019 fish survey caught 522 fish: 16 in Boat Harbour, 104 in wetlands/watercourses and 402 in the estuary. Limited fish retained for some analyses constrained endpoints; PAHs in some tissue samples were above reference/control values. Catch counts are not population estimates; tissue findings need sample-level data and QA/QC |
| 14 | `137895E` | IAAC EIS Appendix X, GHD, *Light Impact Assessment*, 15 January 2020; https://iaac-aeic.gc.ca/050/documents/p80164/137895E.pdf | **B — Browser-rendered 19-page report reviewed**, including seven task tables and receptor comparisons | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-118. Predictive model for seven work stages and nine residential receptors against ILE E2 limits (5 lux pre-curfew; 1 lux after 11 p.m.). Active-remediation scenario maximum is 0.472 lux at a receptor; one pre-curfew task predicts 1.22 lux, below the 5-lux pre-curfew limit. Model assumes 50% light attenuation from directionality/obstruction; exact equipment and locations were unknown. No routine light monitoring proposed; wildlife effects described as poorly understood. The MC225 dredge luminous-flux value is internally inconsistent in the report (15,600 vs 924,000 lm); verify against the original image/workbook before using the equipment model |
| 15 | `137894E` | IAAC EIS Appendix W, WSP, *Baseline Noise Monitoring*, 8 March 2018; https://iaac-aeic.gc.ca/050/documents/p80164/137894E.pdf | **B — Browser-rendered 20-page report reviewed**, including results table and site plan | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-117. Five stations deployed 22 November–20 December 2017; 19 of 28 monitoring days were invalidated by weather, leaving only three complete valid days (72 hours) across all stations plus six days of partial data, with power interruptions also noted. “No exceedance” applies only to valid intervals, not 28 continuous days or a full seasonal baseline |
| 16 | `137893E` | IAAC EIS Appendix V, GHD, *Greenhouse Gas Mitigation Assessment* (22 June 2018) and *Climate Change Resilience Assessment* (22 May 2018); https://iaac-aeic.gc.ca/050/documents/p80164/137893E.pdf | **B — Browser-rendered 2 MB appendix text reviewed**, including both reports and calculation tables | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-119. GHG scenario estimates 368,580 tCO2e baseline (2018–2043) versus 53,500 tCO2e project, a modelled 315,080 tCO2e reduction. The baseline assumes 25 years of continued effluent treatment and methane from the disposal cell; the project scenario assumes waste placement ends by 2024. Climate assessment identifies sea-level rise, extreme high water, storms and precipitation; bridge design uses projected 2100 sea level and current 1-in-100-year storm surge/precipitation assumptions. The climate assessment is qualitative/literature-based, and bridge maintenance under rising sea level/storm surge remained uncertain. These are model scenarios, not measured emissions or verified future performance |


## 52. User's 71-file inventory — additional reviewed item with archaeological confidentiality restriction

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 7 | `137902E` | IAAC EIS Appendix EE, CRM Group 2017 archaeological screening/reconnaissance/shovel testing and Boreas Heritage 2019 Indian Cross Point GPR survey; https://iaac-aeic.gc.ca/050/documents/p80164/137902E.pdf | **B — Browser-rendered Appendix EE text reviewed; key methods, findings and recommendations examined** | **Not A1/A2.** Original 16 MB PDF bytes not downloaded, hashed or preserved | Source BH-116. The 2017 report covers a 141 ha study area and identifies archaeological resources and moderate/high potential areas. The 2019 GPR survey found no burial evidence within four grids inside the existing pipeline right-of-way, but identified unground-truthed anomalies in an adjacent area that could indicate burials. The report recommends archaeological monitoring if the relevant pipeline segment is disturbed. **Critical restriction:** the report says sensitive archaeological site data must not be published or made public without written consent from Nova Scotia’s Coordinator of Special Places. No site coordinates, site IDs, maps or burial locations are reproduced here. Obtain written authorization and PLFN consultation before documentary use. |


## 53. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 6 | `Laboratory+Treatability+Study` | GHD, *Laboratory Treatability Study*, Report 11148275, Report No. 10, 9 April 2018; official project resource PDF: https://static1.squarespace.com/static/5fa9ac321d1bf94e1f13e118/t/5fb2fbd5cce468531e584c73/1605565406097/Laboratory+Treatability+Study.pdf | **B — Full 16-page browser-rendered report reviewed** | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-026 updated. Only three samples (ASB, BH lagoon, estuary) were tested. Initial water exceeded screening criteria for cyanide, TPH and zinc in all three. BH and ASB sediment had multiple exceedances including D/F TEQ (170 and 402 pg/g). Wet geotube dewatering and PAC/RemBind treatment improved results, but BH dewater-water TPH remained 0.178 mg/L against a 0.1 mg/L criterion after PAC treatment. Dry-excavation surface-water treatment still exceeded TPH, lead and zinc. The report concluded wet and dry methods were both bench-scale viable and recommended pilot testing; the later pilot report's finding that dry excavation was ineffective must be reconciled. |


## 54. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 1 | `Supplementary+Phase+2+Study` | GHD, *Supplemental Phase 2 Environmental Site Assessment*, Report 11148275, Report No. 11, 14 September 2018; official project resource PDF: https://static1.squarespace.com/static/5fa9ac321d1bf94e1f13e118/t/5fb2fc6aa269ed475ca25ce7/1605565624084/Supplementary+Phase+2+Study.pdf | **B — Browser-rendered 14,477-line report reviewed**, including main assessment, QA/QC memo and conceptual site model | **Not A1/A2.** Original PDF bytes not downloaded, hashed or preserved | Source BH-037 updated. The 2018 campaign found all five near-mouth Strait sediment samples (NS-SED-3 to NS-SED-7) above PHC criteria, while five background samples 2.5 km east had no sediment exceedances. GHD said further horizontal delineation was required. This is distinct from the 2020 EIS Volume IV's separate five-sample campaign, which reports three PHC screening exceedances. The report's Appendix D lab certificates are not present; the PDF says “to be provided with final.” Groundwater cadmium/chloroform at BHSL-MW-6 and chloroform at EST-MW-2 required confirmation. Pipeline-corridor sampling was deferred because the pipeline was still operating. |


## 55. User's 71-file inventory — original final report not retrieved; related evidence reviewed

| Inventory item | User-supplied filename | Official source identity / locator | Status | Required next action |
|---|---|---|---|---|
| 2 | `Sludge_Thicknes...ping_Final_Rpt (1)` | Build Nova Scotia official resource page lists *Sludge Thickness Determination* as a large Google Drive download; https://boatharbourproject.buildns.ca/resources. Google Drive file ID shown by the official link: `1h-mTHes_jBLzMDt57UZEFGE54J7YJorT` | **A0 + E + C** — official resource listing and file ID confirmed; Google Drive/uc download inaccessible through browser. The final report itself has not been read. Related WSP/SCG presentation BH-171, ESAA 2022 abstract and PLFN 2021 Annual Report reviewed as partial context only | Obtain the actual final report and native LIF/EC point dataset, bathymetric surfaces, top/bottom sludge surfaces, core logs, QA/QC, calibration files, spatial coordinates and volume calculation workbook. Reconcile the presentation's 500 points and 271,000/400,500 m³ estimates with the 2022 abstract's >600 profiles across Boat Harbour/ASB and WSP's ~1 million m³ project-level estimate. Verify “competent sludge” and “transition zone” definitions, spatial extents and uncertainty. Do not mark the user’s final-report file complete based on the conference presentation |


## 49. Cross-source historical review — legislative submissions identify original records but do not replace them

**Additional source BH-198:** Nova Scotia Legislature, Law Amendments Committee submissions on Bill 89 (2015), full browser-rendered 3,214-line composite PDF reviewed: https://nslegislature.ca/sites/default/files/pdfs/committees/62_2_LACSubmissions/Bill89.pdf

This composite contains submissions from different parties. It must not be treated as one neutral account. The PLFN counsel submission provides a detailed chronology and index of underlying historical records. Its key assertions are:
- 25 August 1965: PLFN members raised concerns about loss of clams, quahogs, eels, smelt, lobster and trout; waterfowl feeding grounds; boat anchorage; swimming/recreation; odour; shoreline building lots; and the cultural significance of the harbour. The submission also recounts the 10 October 1965 handwritten agreement after Chief Louis Francis and Councillor Martin Sapier visited the Renforth domestic sewage system. These are the PLFN submission's account; inspect the original memoranda and handwritten instrument before treating this as a definitive record.
- 2 September 1966: PLFN's submission argues that the OIC did not validly transfer riparian rights because the required Indian Act surrender or transfer-in-lieu-of-expropriation procedure had not occurred. It identifies three OIC conditions: remedial action if the harbour became septic, construction of a slipway, and $60,000 compensation. The submission says the compensation was paid but the slipway was not built. This is a party's legal argument and historical account, not a court ruling.
- September 1970: the Province and Scott Maritimes entered a 25-year agreement for the Province to operate the wastewater facility and receive mill wastewater.
- 12 February 1991: the Province's Minister of Environment wrote that the Province had committed to remove the facility within five years and return Boat Harbour to a tidal estuary.
- 20 July 1993: PLFN's counsel argues the Canada–PLFN settlement did not surrender reserve lands or authorize indefinite effluent discharge; this interpretation must be checked against the settlement's full text and any later legal rulings.
- September 1995: PLFN's submission says the Province–PLFN arrangement postponed decommissioning to 31 December 2005 in exchange for non-interference, specified land transfers and cleanup; the associated Province–Scott MOU provided for lease, licence and indemnity arrangements.
- 27 September 2001: PLFN–Kimberly-Clark MOU described a two-stage arrangement: settling basin, emergency spill basin and ASB to remain until 2030, with a proposed bypass pipeline to allow the main stabilization lagoon to be cleaned and returned to tidal conditions. The submission describes annual payments beginning at $200,000 and increasing to $280,000 by 2030, and forest-land transfer after pipeline construction. It says the Province extended the mill lease to 2030 in 2002; the pipeline was not built by the original 2005 deadline; a 2 January 2006 amendment extended the deadline to 31 December 2008; PLFN refused another extension in November 2008; and the Province confirmed a closure/relocation/cleanup commitment on 4 December 2008.
- The index identifies the primary records that must be obtained: 1966 OIC; 1965 meeting memoranda and handwritten agreement; 1970 MacDonald/Ferguson/other letters; 1995 MOU and associated agreements; 2001 MOU; 2002 lease extension; 2006 amendment; and 2008 letters.

**Effect on the 71-file audit:** this improves contextual understanding for inventory items 44–62, but does not upgrade their original-document status. Items 45–50 (2008/2002/1995 agreements), 51–52 (1989/1986 pleadings), and 53–62 (1970/1966/1965 letters and orders) remain C until their own originals are actually read. Do not conflate the late-2008 proposed Accommodation Agreement with the Province's 4 December 2008 closure commitment; they are distinct records.
