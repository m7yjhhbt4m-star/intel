# Independent Monitoring — Technical Design and Method Selection

**Status:** Proposed technical framework informed by the initial research dossier; not an approved field protocol.  
**Geographic scope:** Boat Harbour/A’se’k, all relevant associated wetlands and waterways, estuary, Northumberland Strait receiving waters, and defensible regional reference areas.  
**Media:** Water and sediment are mandatory; biota is a complementary line of evidence where permissions and study design support it.

## 1. Monitoring objectives

1. Independently characterize current water and sediment conditions in and around the former treatment facility.
2. Resolve historical sampling gaps, especially sediment depth and spatial coverage.
3. Characterize wetlands as distinct receiving environments rather than assuming lagoon results represent them.
4. Assess whether measurable contaminant gradients or transport pathways extend into the estuary and Northumberland Strait.
5. Establish a repeatable baseline and time series that can distinguish seasonal variability, storm events, remediation effects and long-term change.
6. Independently evaluate project monitoring claims and model predictions using transparent, reproducible methods.

## 2. Spatial design — proposed strata

Do not choose fixed station coordinates until historical datasets, property access, bathymetry, Indigenous direction and current project constraints have been reviewed.

| Stratum | Target coverage | Purpose |
|---|---|---|
| A. Main Boat Harbour lagoon | Multiple depositional zones, shoreline margins, former discharge influence, inlet/outlet areas | Current water/sediment chemistry; depth profile; sediment thickness |
| B. Treatment infrastructure / former settling areas | Twin settling basins, former settling ponds, aeration/stabilization areas, ditches and channels where accessible | Source-area delineation and pathway assessment |
| C. Adjacent wetlands | All 25 wetlands identified in project literature, subject to access and prioritization; stratify historical discharge exposure, current hydrology and reference status | Sediment/water/biota gradients and wetland condition |
| D. Estuary and tidal connection | Estuary channel, marsh/salt-marsh complex, dam/bridge influence and transition zone | Freshwater-to-marine transition, sediment transport and tidal mixing |
| E. Near-field Strait | Preserve comparable 2020 study stations and add stations around discharge/estuary mouth | Validate baseline and investigate near-field spatial gradients |
| F. Mid-/far-field Strait | Extend beyond the 2020 two transects and 8 km mussel coastline footprint, using hydrodynamic and habitat rationale | Test broader distribution and background |
| G. Regional reference areas | Multiple reference stations outside plausible site influence but with comparable sediment type, depth, exposure and habitat | Distinguish site-related signals from natural regional background |

**Important:** “Entire Northumberland Strait” is the user's geographic ambition, not a scientifically meaningful instruction to sample every square kilometre. The field design should cover the full receiving-water region relevant to plausible transport pathways, with regional reference stations and a defensible spatial-statistical design. A full basin-wide survey would be a separate scale and budget decision.

## 3. Water sampling and in-situ measurements

### Field measurements
Use calibrated multiparameter sondes at each sampling event for:
- Temperature
- pH
- Specific conductivity/salinity
- Dissolved oxygen
- Turbidity
- Oxidation-reduction potential where relevant
- Water depth

Collect water samples at surface and, where depth/stratification justifies it, near-bottom. Include tidal phase, current direction, weather, recent precipitation, water level, sample depth, GPS, and time.

### Laboratory water analyses
Select analytes based on historical findings and source/pathway rationale:
- Dissolved and total recoverable metals: As, Cd, Cr, Cu, Pb, Hg, Zn, plus other metals indicated by Phase II data.
- Total mercury and methylmercury as separate analytes where relevant.
- Suspended solids / total suspended solids.
- Dissolved organic carbon, total organic carbon where appropriate, nutrients and general chemistry.
- PAHs, petroleum hydrocarbons, VOCs, dioxins/furans, PCBs, and resin/fatty acids only where source history and previous detections justify them.
- Field and laboratory blanks, duplicates, matrix spikes and certified reference materials.

Use accredited laboratories and request reporting limits below the relevant comparison criteria. Specify dissolved versus total fractions before collection; filtration, preservation, containers and holding times must follow the laboratory's method requirements.

## 4. Sediment sampling

### Surface sediment
Use grabs (e.g., Ponar or equivalent) for surficial sediment at locations suitable for the substrate and vessel. Record sample recovery, sediment texture, colour, odour (without treating odour as chemical proof), shell/organic content, water depth and GPS.

### Cores
Use gravity, percussion or vibracoring methods selected for sediment type, depth and access. The historical dataset is heavily weighted to 0–15 cm, so the new design must explicitly characterize vertical profiles. Potential intervals should be chosen after pilot coring; do not prescribe universal intervals before sediment stratigraphy and analytical requirements are known.

### Core logging and analyses
- Photograph and log each core before subsampling.
- Preserve discrete depth intervals; do not homogenize the entire core.
- Analyze sediment grain size, total organic carbon and relevant geochemistry to interpret contaminant binding and bioavailability.
- Analyze metals/metal(loid)s, total Hg, MeHg, PAHs, petroleum hydrocarbons, PCDD/PCDF, PCBs and other compounds according to site-specific evidence.
- Record dry-weight basis, detection limits, laboratory method, sample recovery and QA/QC.

### Sediment transport and bathymetry
Use single-beam or multibeam bathymetry as scale and depth allow; side-scan sonar for bottom texture/targets; sub-bottom profiling where sediment thickness/stratigraphy can be resolved and the acoustic conditions support it. Sonar does not identify chemical composition. Calibrate sediment-thickness interpretation with cores.

## 5. Drone and remote sensing workstream

### Platform and sensors
Start with RGB imagery and a properly calibrated multispectral sensor for repeatable orthomosaics, shoreline/wetland mapping and vegetation condition. Hyperspectral equipment should be considered only after a pilot demonstrates a defined decision value that cannot be achieved with simpler sensors.

### Valid use cases
- Map visible surface-water plume boundaries and relative turbidity patterns.
- Estimate TSS/turbidity or chlorophyll proxies using locally calibrated models and concurrent water samples.
- Map wetland vegetation condition and change.
- Identify exposed sediment, erosion, shoreline change and surface anomalies.
- Provide georeferenced repeat imagery for change detection and sampling design.

### Invalid claims
- Do not claim that optical drone imagery directly identifies dissolved metals, mercury species, PFAS, dioxins/furans or specific chemical concentrations.
- Do not infer submerged sediment chemistry from a water-surface spectral signature.
- Do not interpret model output as laboratory measurement.
- Do not infer contaminant source or direction of movement from a single image.

### Calibration and validation
Every remote-sensing campaign used for quantitative water-quality inference must be paired with field observations and lab samples across the observed range of water conditions. Maintain sensor calibration records, reflectance panels/irradiance measurements as appropriate, flight altitude, overlap, sun angle, tide, weather, water level, sensor settings, georeferencing and processing workflow. Use independent validation samples rather than assessing a model only on its training samples.

## 6. Biota and food-web indicators

The 2020 Strait baseline and 2021 wetland study demonstrate the value and limits of biota as a separate line of evidence. Potential taxa include lobster, rock crab, blue mussels and selected benthic invertebrates, but species, locations, tissue type, sample size, timing and collection methods must be designed with DFO permits, PLFN direction and relevant authorities.

Mercury speciation matters: total Hg and methylmercury are not interchangeable. Arsenic speciation may also be required before drawing food-safety conclusions from total arsenic results. Do not collect country foods or culturally important species without appropriate consent, permits, protocols and clear data governance.

## 7. Analytical methods — selection principles

Methods previously identified as relevant include:
- ICP-MS for multi-element metals.
- Cold-vapour atomic absorption/fluorescence or validated equivalent for total mercury.
- Methylmercury-specific preparation and analytical methods (e.g., ethylation with CVAFS or validated equivalent).
- GC-MS / GC-MS/MS for PAHs, petroleum hydrocarbons and VOCs as appropriate.
- High-resolution GC-MS / HRMS for dioxins and furans.
- Suitable validated methods for PCBs, resin/fatty acids and general chemistry.

These are candidate method families, not final method specifications. Obtain laboratory method sheets, accreditation scope, sample container/preservation requirements, detection limits, holding times, uncertainty and costs before finalizing the sampling plan.

## 8. QA/QC, custody and data integrity

Minimum proposed controls:
- Unique immutable sample IDs linked to coordinates, date/time, medium, depth, station stratum and collection method.
- Chain-of-custody forms from field collection to laboratory receipt.
- Field duplicates, equipment blanks, trip blanks where VOCs apply, field blanks, laboratory method blanks, matrix spikes and certified reference materials at frequencies specified in the QA project plan.
- Calibrated instruments with pre-/post-deployment checks.
- Documented deviations, failed samples, rejected samples and detection-limit changes.
- Preserve original instrument files, imagery, laboratory certificates, chromatograms/spectra where available, GPS tracks, processing parameters and analysis code.
- Separate raw data, corrected data and derived/modelled products.
- Version all datasets and publish machine-readable metadata where permitted.
- Never silently overwrite or discard an original measurement.

## 9. Data and analysis architecture

Recommended open stack:
- QGIS for spatial review and map production.
- PostGIS for canonical spatial observations and station/sample relationships.
- GeoPackage/CSV/Parquet for exchange and archival exports.
- Reproducible scripts/notebooks for QA/QC, statistics, interpolation and remote-sensing calibration.
- Version-controlled source register and methods documents.

Each observation should retain:
- Source and sample identifier.
- Coordinate reference system and coordinate accuracy.
- Collection date/time, tide and weather.
- Medium, depth, method and field observations.
- Analyte, result, units, fraction, detection limit and qualifier.
- Laboratory, method, accreditation, QA/QC status and uncertainty.
- Applicable benchmark and benchmark version.
- Provenance and revision history.

Do not map below-detection values as zero. Do not interpolate across disconnected water bodies or sediment environments without a defensible model. Distinguish measured values from interpolations and remote-sensing estimates.

## 10. Sampling cadence — proposed, subject to pilot

A credible programme should combine:
- A baseline round across the selected strata.
- Seasonal repeat rounds to capture seasonal hydrology and biological variation.
- Event-based sampling after major rainfall, runoff or other events likely to mobilize sediment.
- Tidal-stage sampling in the estuary and near-field marine area.
- Higher-frequency TSS/turbidity and water-level logging during any active remediation/dam-removal period.
- Post-event sampling to track deposition and recovery.

Exact cadence and station counts should be set only after reviewing existing monitoring datasets, access, statistical power, lab costs and project schedule. Do not claim a monitoring frequency is adequate without a power/design rationale.

## 11. Permits, rights and governance

Before fieldwork:
- Engage Pictou Landing First Nation and follow its direction on research purpose, access, cultural protocols, data ownership, interpretation, publication and sensitive locations.
- Obtain land access and permissions from the relevant landholders.
- Confirm Transport Canada / NAV CANADA / aviation requirements for drone operations and any restricted airspace.
- Confirm DFO scientific licences and Fisheries Act requirements for fish, shellfish, aquatic species and habitat work.
- Confirm provincial and federal permits for sediment/water sampling, wetlands, wildlife, navigation and protected areas as applicable.
- Coordinate with current remediation authorities to avoid interference with project operations and preserve independence.
- Establish independent QA/QC review and conflict-of-interest disclosures.

This document is not legal advice and does not replace regulator/rights-holder consultation.

## 12. Pilot sequence

1. Recover original historical datasets, station coordinates, laboratory certificates, and assessment appendices.
2. Build a GIS of all historical stations, study boundaries, wetlands, shoreline, outfalls, channels, bathymetry and reference locations.
3. Identify gaps by medium, analyte, depth, date and spatial stratum.
4. Select a small pilot spanning lagoon, wetland, estuary, near-field Strait and a reference area.
5. Run paired drone/field/lab observations to test whether optical metrics add useful information.
6. Pilot grab/core recovery and sonar interpretation against measured sediment thickness.
7. Review QA/QC, laboratory reporting limits, costs and statistical power.
8. Revise the full sampling design before procurement or deployment.

## 13. Decision gates

- **Gate 1 — Evidence recovery:** No final station plan until historical data and spatial coordinates have been assembled.
- **Gate 2 — Governance/access:** No field deployment until permissions and PLFN engagement protocols are established.
- **Gate 3 — Method validation:** No quantitative drone water-quality claims until locally calibrated and independently validated.
- **Gate 4 — Lab readiness:** No sampling event until containers, preservation, holding times, detection limits and chain-of-custody are confirmed with the laboratory.
- **Gate 5 — Scale-up:** No full programme procurement until pilot results demonstrate that each instrument/method contributes measurable value.

## Key technical sources

- IAAC (2025), Environmental Assessment Report: https://iaac-aeic.gc.ca/050/evaluations/proj/80164/document/160559?culture=en-CA
- Hoffman et al. (2017), DOI 10.1007/s10661-017-5952-0: https://doi.org/10.1007/s10661-017-5952-0
- Chaudhary et al. (2020), DOI 10.1016/j.marpolbul.2020.111372: https://doi.org/10.1016/j.marpolbul.2020.111372
- Quanz et al. (2021), DOI 10.1007/s11273-020-09779-0: https://doi.org/10.1007/s11273-020-09779-0
- Jaywant & Arif (2024), DOI 10.3390/s24248041: https://doi.org/10.3390/s24248041
- Supplementary Phase II ESA: https://static1.squarespace.com/static/5fa9ac321d1bf94e1f13e118/t/5fb2fc6aa269ed475ca25ce7/1605565624084/Supplementary+Phase+2+Study.pdf
