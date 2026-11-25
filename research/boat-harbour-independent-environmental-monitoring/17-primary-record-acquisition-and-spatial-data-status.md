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
| 6 | `Laboratory+Treatability+Study` | GHD, *Laboratory Treatability Study*, Report 10, Project 11148275, 9 April 2018; official project-hosted PDF: https://static1.squarespace.com/static/5fa9ac321d1bf94e1f13e118/t/5fb2fbd5cce468531e584c73/1605565406097/Laboratory%2BTreatability%2BStudy.pdf | **B — Full browser-rendered PDF text reviewed**, including report body and analytical tables | **Not A1/A2.** Original PDF bytes not downloaded to evidence storage, hashed or preserved | Source recorded as BH-114 in Document 05. Key limitation: bench-scale tests based on samples from three site areas collected in 2017; not current monitoring or full-scale validation. The user’s local phone copy was not accessed. |


## 16. User's 71-file inventory — additional reviewed item

| Inventory item | User-supplied filename | Identified source | Online review status | Binary preservation status | Review note |
|---|---|---|---|---|---|
| 1 | `Supplementary+Phase+2+Study` | GHD, *Supplemental Phase 2 Environmental Site Assessment*, Report 11, Project 11148275, 14 September 2018; official PDF: https://static1.squarespace.com/static/5fa9ac321d1bf94e1f13e118/t/5fb2fc6aa269ed475ca25ce7/1605565624084/Supplementary%2BPhase%2B2%2BStudy.pdf | **B — Full browser-rendered report reviewed**, including main report, sample-location figures, borehole/well logs, embedded QA/QC/data-verification memo and conceptual site model figures | **Not A1/A2.** Original PDF bytes not downloaded to evidence storage, hashed or preserved | Source recorded as BH-115 in Document 05. Important unresolved items: vertical elevations for seven new wells were not surveyed, so no hydraulic gradients could be calculated; Northumberland Strait near-estuary PHC exceedances remained horizontally undelineated; deeper FSP2/FSP3 sediment delineation remained incomplete; confirmation sampling was recommended at BHSL-MW-6 and EST-MW-2. Appendix D (laboratory certificates) is explicitly marked “to be provided with final” and is absent from this copy. The user’s local phone copy was not accessed. |
