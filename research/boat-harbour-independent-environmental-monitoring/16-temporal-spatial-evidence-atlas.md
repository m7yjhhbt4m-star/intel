# Temporal Spatial Evidence Atlas — Boat Harbour / A’se’k
**Document:** 16  
**Version:** 1.0 — 23 November 2026  
**Purpose:** Define the evidence model, source inventory and acquisition requirements for dated 2D/3D reconstruction of Boat Harbour, connected waterways, Pictou Harbour and the Northumberland Strait receiving environment.

## 1. Non-negotiable cartographic rule

The atlas must show what the evidence supports at a stated date—not create a visually persuasive but historically false reconstruction. Every mapped feature must carry a source, date basis, spatial precision, method and uncertainty label. A feature shown on a map is not automatically a verified fact.

The atlas must distinguish:
- **valid time:** when a physical condition or event existed;
- **record time:** when a document, measurement or observation was created or published;
- **observation time:** when imagery, a sample, survey or instrument reading was acquired;
- **model time:** the simulated time represented by a model output.

Do not substitute report publication date for field-survey date. Do not interpolate a shoreline, well location, contaminant plume or facility footprint across periods without a documented method and uncertainty statement.

## 2. First confirmed spatial-temporal anchor: 2016 topo-bathymetric survey

**Source:** Webster, Collins & Vallis (2017), Applied Geomatics Research Group, Nova Scotia Community College, *Topo-Bathymetric Lidar Research to support Remediation of Boat Harbour: Final Report*.  
URL: https://www.nscc.ca/appliedresearch/docs/geomatics-psc-ns-lands-finalreport-mar2017.pdf  
Canonical source-register record: BH-031.

### Confirmed from the report
- Airborne topo-bathymetric lidar survey of Boat Harbour / outer Pictou Harbour took place **7 September 2016, 13:15–14:50 UTC**, with 19 flight lines.
- Ground-truth collection was conducted in **August 2016**.
- An Acoustic Doppler Current Profiler (ADCP) was deployed **11 August 2016** and recovered **13 September 2016**, approximately 35 days of current and water-level observations.
- Products described include a lidar point cloud, digital elevation/surface models, orthophoto mosaic, seabed reflectance, bottom-type classification, and a hydrodynamic model.
- The lidar survey reached a minimum reported elevation of **−4.8 m CGVD28**. The report describes merging with Canadian Hydrographic Service 5 m multibeam data where lidar did not penetrate.
- Validation statistics reported by the authors: land RTK validation mean difference −0.14 m, standard deviation 0.04 m; bathymetric validation mean difference −0.17 m, standard deviation 0.25 m; CHS 5 m multibeam comparison mean difference −0.03 m, standard deviation 0.30 m.
- The authors report the hydrodynamic model captured broad circulation patterns but identify limitations: east-west current amplitude was not consistently reproduced; north-south current phase was wrong in parts of the comparison; flow measurements at the Pictou Causeway and a spatially varying bed-resistance map could improve the model.
- The report describes a dark plume at the Boat Harbour outlet that prevented lidar penetration. This is an optical/laser observation, not chemical identification or proof of a contaminant concentration.

### Critical licensing / acquisition limitation
The report's copyright section states AGRG/NSCC retains ownership of data collected using its equipment and related processing IP. It permits unlimited copies for internal use and derived graphics/hardcopy with the acknowledgement “Data acquired and processed by the Applied Geomatics Research Group, NSCC”; it also states the data and associated IP will not be shared without AGRG/NSCC permission. **Do not redistribute the underlying point cloud, DEM, orthophoto or derived GIS datasets until the licence/permission is confirmed in writing.** A public report PDF is not the same thing as permission to redistribute its underlying datasets.

### What is not yet acquired
The report has been examined through its accessible full-text rendering, but the original PDF binary and the deliverable datasets (LAZ/LAS, DEM/DSM, orthophoto, bottom-type vectors, ADCP time series, hydrodynamic model inputs/outputs and survey control) have not been downloaded, hashed or placed in a controlled vault. The report's figures are useful for planning and cross-checking, but digitizing a figure is not equivalent to obtaining its underlying georeferenced data.

## 3. Provincial geospatial sources identified

### 3.1 Nova Scotia DataLocator / Aerial Photography Library
- DataLocator: https://nsgi.novascotia.ca/datalocator/
- GeoNOVA base mapping: https://geonova.novascotia.ca/base-mapping
- Aerial-photo library overview: https://geonova.novascotia.ca/sites/default/files/resource-library/Aerial-photography_2015_NEW.pdf
- GeoNOVA reports historical analog aerial photography from **1950–2012** is being scanned; the DataLocator indexing system identifies photo centres and allows filtering by year/type. The official inventory and actual Boat Harbour frame availability must be queried and recorded.
- GeoNOVA describes orthophotography as geometrically corrected and mosaicked imagery, with provincial 20 cm imagery products in some coverage areas. Acquisition year, ground sample distance, orthorectification metadata and licensing must be recorded for each tile.
- June 2026 GeoNOVA release states new imagery from **2024 for Eastern Nova Scotia (16,334 km²)** and **2025 for southwestern Nova Scotia (8,851 km²)** is available for selected areas. This does not yet prove which Boat Harbour tiles are covered; confirm exact tile footprints, image dates and metadata through DataLocator before using them as a time slice.
- GeoNOVA source: https://geonova.novascotia.ca/new-orthophotography-now-available

### 3.2 LiDAR / terrain
- Elevation Explorer: https://nsgi.novascotia.ca/datalocator/elevation
- The provincial service describes downloadable classified LiDAR point clouds as LAZ in NAD83(CSRS)v6 / UTM Zone 20 / CGVD2013, and derived DEM/DSM/hillshade/CHM/intensity products as GeoTIFF. Products are tile-based.
- The service reports multiple acquisition years and tile footprints. Its general availability does not establish coverage at the project site. Query the index for Boat Harbour and record each tile's acquisition year, sensor, resolution, vertical datum, classification and licence.
- **Datum warning:** the 2016 AGRG report's derived heights are described relative to CGVD28, while the current provincial Elevation Explorer describes CGVD2013. Do not overlay elevations until the vertical datum transformation is documented and applied. Preserve original values and datums.

### 3.3 Hydrography
- GeoNOVA states the Nova Scotia Hydrographic Network (NSHN) is the authoritative provincial source for inland surface water and includes lakes, rivers, islands, swamps, coastlines, ditches, dams, dykes, reservoirs, canals, flow direction and network attributes.
- Source: https://geonova.novascotia.ca/news-blog/nova-scotia-hydrographic-network-now-available
- Obtain the actual versioned vector data and metadata. Do not assume its current shoreline/watercourse geometry represents 1967 or another historic date.

### 3.4 2016 topo-bathymetric and hydrodynamic products
The 2017 AGRG report is unusually valuable because it provides a site-specific 2016 baseline with topography, bathymetry, seabed classification, orthophotos and tidal-current model outputs. It is a high-priority source for a 2016 scene, subject to data access and licence. Its model is an outer Pictou Harbour / Boat Harbour outlet baseline, not a validated model of the entire Northumberland Strait.

## 4. Proposed dated map scenes

| Scene date / period | Candidate layers | Evidence status | What must not be implied |
|---|---|---|---|
| Pre-1967 (choose exact image year after archive search) | Historic aerial frames, chart/shoreline, natural tidal inlet, historic maps | Not yet acquired for Boat Harbour; historical reconstruction required | Do not present a modern shoreline as the pre-industrial shoreline |
| 1965–1967 transition | Dated aerial frames, Order-in-Council records, causeway/dam/berm construction records, mill and pipeline plans | Historical event reported in later records; primary construction drawings and exact dates not yet recovered | Do not infer exact construction sequence from the year “1967” alone |
| 2003–2011 wellfield period | Old/new PLFN wellfield, well construction and pumping records, Dillon 2003 and 2011 reports, water levels and chemistry | Source titles identified in EIS references; underlying reports/data not yet recovered | Do not draw capture zones from well locations alone |
| August–September 2016 | AGRG lidar/orthophoto, ground-truth points, ADCP observations, modelled tidal currents | Site-specific report examined; original data files not acquired | Model vectors are model outputs, not direct continuous observations everywhere |
| 2017–2018 baseline | EIS monitoring-well network, sample locations, groundwater levels, chemistry, surface-water stations, sediment/biota stations | EIS summaries reviewed; raw source reports, lab certificates and all coordinates incomplete | Do not interpolate contaminant concentrations between sampled points without a defensible model |
| 2020 EIS publication state | EIS figures, study-area boundaries, site features, wells and baseline maps | EIS Volume IV text reviewed; figure source data not fully extracted | EIS project boundaries are not necessarily legal parcel boundaries |
| 2024–2025 assessment/decision | Final project design footprint, study areas, monitoring conditions and dated imagery if coverage confirmed | IAAC 2025 EA report and Decision Statement examined | Decision/approved design is not proof that construction or monitoring occurred |
| 2025 reporting period / 2026 publication | Status and activities from 2025 Annual Report, dated 30 March 2026 | Registry metadata and secondary catalogue summary located; official report body not yet reviewed | Do not use the secondary abstract as a substitute for the official report |
| 2026 | Current orthophoto, current provincial hydrography, alternative-site context, current monitoring records | Some provincial sources identified; site-specific tile and record retrieval outstanding | A possible alternative site is not a selected site |

## 5. Required layer inventory

### A. Base geography and terrain
1. Current orthophoto tiles, with image acquisition dates and metadata.
2. Historical aerial photo frames, scanned originals and georeferencing control.
3. LiDAR point clouds and DEM/DSM products by acquisition year.
4. Bathymetry and hydrographic chart soundings, with survey date and vertical datum.
5. Coastline and intertidal boundaries by observation date and tide stage.
6. Streams, ditches, wetlands, ponds, dams, dykes, culverts and drainage catchments.
7. Elevation contours and slope derived from source DEMs, with processing lineage.

### B. Industrial and remediation infrastructure
1. Historic estuary and harbour footprint.
2. Effluent-treatment facility basins and process cells.
3. Causeway, dam, dykes, bridges, culverts and shoreline protection.
4. Industrial outfalls, pipelines, pumping stations and former discharge points.
5. Existing containment-cell footprint, design stages and capacity changes.
6. Remediation work areas, dredge cells, temporary storage, dewatering/geotextile areas, treatment and discharge points.
7. Any candidate alternative-site polygons, clearly marked as proposed/assessed/not selected unless a formal decision establishes otherwise.

### C. Groundwater
1. Every well and piezometer with original well ID, coordinates, coordinate source, elevation, total depth, casing, screen/open-hole interval, lithology, hydrostratigraphic unit and construction date.
2. Pumping wells PW9/PW10 and other production wells, pumping periods, flow rates, water levels and operational status.
3. Surveyed groundwater elevations with measurement date/time, reference datum, measuring point and instrument/method.
4. Potentiometric surfaces only where same hydrostratigraphic zone and same survey window support contouring.
5. Hydraulic conductivity/transmissivity tests with test dates, method, interval and raw time series.
6. Groundwater chemistry sample events and results with lab, method, units, detection limits, qualifiers and certificates.
7. Surface-water/groundwater interaction points and temperature observations, if actually measured.
8. Capture-zone boundaries only as dated model outputs, with model version, pumping assumptions, calibration, uncertainty and source files.

### D. Surface water, sediment, marine and ecology
1. Surface-water sampling points and time series.
2. Sediment cores/grabs with sample depth, date, coordinates, tide and station metadata.
3. Dredging/removal footprints, volumes and dates, if measured.
4. Turbidity/TSS monitoring points and event records.
5. ADCP deployments, current vectors, water levels, tide predictions and model outputs.
6. Benthic habitat, eelgrass/submerged aquatic vegetation and ground-truth points.
7. Marine sediment and biota stations in Pictou Harbour and Northumberland Strait.
8. Country-food sampling locations only under rights-holder-approved governance and access controls.

### E. Administrative / rights-holder context
Map administrative study areas, reserve boundaries and public infrastructure only from authoritative, appropriately licensed records. Do not publish sensitive Indigenous knowledge, cultural sites, burial locations, interview-derived traditional-use locations, private well coordinates or personal information without explicit authorization and governance approval.

## 6. Geospatial database structure

Use a spatial database with explicit temporal validity and provenance. Suggested logical tables:

- `source_document`: source ID, title, author, issuer, document date, version, URL, file name, MIME type, licence/rights, acquisition status, SHA-256, original/derivative flag.
- `source_asset`: file path/object key, media type, byte size, hash, page/figure/table locator, extraction method, OCR status.
- `spatial_feature`: stable feature ID, geometry, geometry type, horizontal CRS, vertical CRS, location method, positional accuracy, geometry source.
- `feature_validity`: feature ID, valid_from, valid_to, date precision, temporal basis, uncertainty.
- `observation_event`: event ID, observation date/time/time zone, campaign, operator, method, instrument, conditions, QA/QC status.
- `sample_event`: sample ID, parent sample, medium, depth interval, collection method, chain-of-custody reference, laboratory, analytical batch.
- `analytical_result`: sample ID, analyte, result, unit, fraction, detection/reporting limit, qualifier, method, guideline/version (if compared), lab certificate.
- `well_construction`: well ID, casing, screen/open-hole interval, total depth, lithology, elevation and source.
- `water_level`: well ID, timestamp, measured level, measuring-point elevation, datum, pumping state and method.
- `model_run`: model ID/version, input sources, calibration period, assumptions, scenario, time step, outputs, validation and uncertainty.
- `claim_link`: claim ID, source ID, exact page/figure/table, claim type, attribution, review status and reviewer.
- `rights_access`: access class, consent/authority, permitted purpose, disclosure restriction and review date.

Store original source files unchanged. Normalized GIS layers and extracted tables are derivatives with their own hashes and transformation logs. A database row must point back to the original page, figure, sample ID or raw data record.

## 7. Required time-aware display rules

- A dated layer must show its observation date and source in the legend or feature inspection panel.
- Use distinct symbology for measured locations, modelled fields, interpreted boundaries, proposed footprints and unverified locations.
- Show uncertainty/accuracy as an explicit attribute; avoid false precision in labels.
- Use separate vertical datums or transform them with a documented geodetic operation.
- Never display a modelled current or groundwater-flow arrow as a measured vector.
- Never display a sample result as a continuous plume unless a validated spatial model supports that surface.
- Do not connect separate monitoring campaigns into a continuous time series unless methods, stations, analytes and comparability have been checked.
- Keep restricted Indigenous/cultural layers in a separately permissioned workspace; default to hidden and non-exportable until approved.

## 8. First practical deliverable

The first defensible visual package should be a sequence of dated, clearly captioned 2D map views, not a speculative animated 3D reconstruction:

1. **Historical baseline:** earliest suitable pre-1967 aerial photograph or map, only after exact frame date and provenance are confirmed.
2. **2016 baseline:** AGRG orthophoto and topo-bathymetric surface, with 2016 survey date and datum shown.
3. **2017–2018 monitoring:** wells and actual sampling locations, each with date and media; do not draw unsupported concentration surfaces.
4. **2020 EIS state:** source-derived study-area and infrastructure features, clearly labelled as EIS mapping.
5. **2024/2025/2026 current context:** imagery only where tile coverage and acquisition dates are verified, plus project status layers sourced from dated official records.

3D terrain can follow once the actual LiDAR/DEM files, datum transformations and licences are secured.

## 9. Open acquisition tasks
- Obtain all Boat Harbour DataLocator aerial-photo frame IDs, scan files, flight dates, camera metadata and rights.
- Confirm the exact 2024 orthophoto coverage and tile IDs for Boat Harbour; acquire original GeoTIFFs and metadata.
- Query the provincial Elevation Explorer for site-specific LiDAR tile footprints, acquisition years and LAZ/GeoTIFF download links.
- Obtain the 2016 AGRG/NSCC raw and processed deliverables, ADCP time series, survey control, model grids and licence/permission.
- Obtain Canadian Hydrographic Service historical chart and multibeam survey data with dates, soundings and vertical datum.
- Recover the full EIS Appendix Z (230 MB) and extract AECOM 2016, GHD 2018 and related well logs/figures/model appendices.
- Obtain the Dillon 2003 and 2011 groundwater reports and the original wellfield construction/pumping records.
- Obtain the complete EIS monitoring-well inventory and sample coordinates, lab certificates and raw data tables.
- Obtain provincial approval instruments and approved monitoring plans before mapping any claimed monitoring obligations or compliance history.
- Obtain rights-holder direction before mapping or disclosing sensitive Indigenous knowledge.

## 10. Source references
- AGRG/NSCC 2017 report: https://www.nscc.ca/appliedresearch/docs/geomatics-psc-ns-lands-finalreport-mar2017.pdf
- GeoNOVA base mapping: https://geonova.novascotia.ca/base-mapping
- GeoNOVA 2026 orthophoto release: https://geonova.novascotia.ca/new-orthophotography-now-available
- Nova Scotia DataLocator: https://nsgi.novascotia.ca/datalocator/
- Elevation Explorer: https://nsgi.novascotia.ca/datalocator/elevation
- Nova Scotia Hydrographic Network: https://geonova.novascotia.ca/news-blog/nova-scotia-hydrographic-network-now-available
- EIS Volume IV: https://iaac-aeic.gc.ca/050/documents/p80164/137222E.pdf
- EIS Appendix Z: https://iaac-aeic.gc.ca/050/documents/p80164/137897E.pdf
- EIS registry index: https://iaac-aeic.gc.ca/050/evaluations/proj/80164/document/137959
- 2025 Annual Report registry record: https://iaac-aeic.gc.ca/050/evaluations/exploration?culture=en-CA&projDocs=80164


## 11. Second confirmed map anchor: 2020 EIS groundwater mapping

EIS Volume IV contains a set of dated groundwater and site maps that can form a separate **2020 documentary map scene**. Source: GHD, Environmental Impact Statement, Volume IV, 17 November 2020. Official PDF: https://iaac-aeic.gc.ca/050/documents/p80164/137222E.pdf. Existing source-register ID: BH-038.

Confirmed from the EIS text and figure register:
- Figure 7.1-12: Containment Cell Monitoring Network.
- Figure 7.1-13: Groundwater Elevations Associated with the Containment Cell Versus Time.
- Figure 7.1-14: PLFN Well Field — Location of Water Supply Wells and Monitoring Wells. The figure itself is dated **17 August 2020** and identifies its coordinate system as **NAD 1983 CSRS UTM Zone 20N**.
- Figures 7.1-15 and 7.1-16: PLFN overburden and shallow-bedrock groundwater elevations versus time.
- The EIS states containment-cell groundwater elevations were typically measured quarterly from **1995 through 2019**.
- The EIS includes summary statistics and hydrographs for containment-cell and PLFN wellfield monitoring wells. The plotted hydrographs and summary statistics are not a substitute for the underlying time-stamped water-level records.

### What this adds to the time-based atlas
The EIS provides a 2020-dated map of the PLFN wellfield's supply and monitoring wells and a historical time-series context reaching back to 1995 for the containment-cell monitoring network. This makes it possible to plan at least two evidence-based spatial scenes:
1. **2016 survey scene:** AGRG topo-bathymetric surface, orthophoto and hydrodynamic baseline (subject to native-data permission).
2. **2020 EIS scene:** EIS source-mapped containment-cell and PLFN wellfield monitoring networks, with the 17 August 2020 figure date and NAD83(CSRS) UTM Zone 20N coordinate system explicitly shown.

The map geometry must be digitized from the original EIS figures only after the figure image is obtained and georeferenced. Store digitized features as **derived/interpretive geometry**, with source figure, digitizer, control points, transformation method, residual error and uncertainty. Do not claim surveyed coordinates if the source provides only a map symbol or approximate location.

### Critical data gap
The EIS text identifies the map and hydrographs but the raw time-series, original well inventory, construction logs, surveyed coordinates, measuring-point elevations and source GIS project have not been acquired. Retrieve the underlying EIS Appendix Z reports, Dillon 2003/2011 groundwater reports, AECOM 2016, GHD 2018 and provincial annual reports before attempting a complete historical groundwater animation.
