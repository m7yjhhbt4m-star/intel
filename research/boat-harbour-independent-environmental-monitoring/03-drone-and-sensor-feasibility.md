# Drone and Sensor Feasibility — Boat Harbour / A’se’k

**Version:** 2.0 — technical evidence review, 21 November 2026  
**Question:** Can a drone equipped with multispectral or hyperspectral sensors detect chemicals in Boat Harbour water and sediment?

## 1. Direct answer

**Not in the way a chemical laboratory does.** A drone can map optical properties and environmental patterns that may correlate with certain water-quality parameters. It cannot directly identify and quantify most individual contaminants of concern at environmentally relevant concentrations in natural water, and it cannot determine the chemistry of submerged sediment.

The correct role is reconnaissance, spatial mapping, repeat monitoring and sample targeting. Laboratory analysis of collected water, sediment and tissue remains essential.

## 2. What the optical sensors measure

Passive RGB, multispectral and hyperspectral sensors measure reflected sunlight across wavelength bands. The measured signal is influenced by:
- water absorption and scattering;
- suspended particles and turbidity;
- chlorophyll and other pigments;
- coloured dissolved organic matter;
- water depth and bottom reflectance;
- surface roughness, sun glint and viewing geometry;
- atmospheric conditions and sensor calibration.

Hyperspectral sensors collect many narrow bands and can resolve more spectral structure than conventional multispectral sensors. More bands do not automatically mean direct detection of a dissolved chemical.

## 3. Parameter feasibility

| Target / condition | Drone optical feasibility | What is actually defensible |
|---|---|---|
| Surface plume / visible discolouration | Good for mapping visible patterns | Map anomaly and extent; collect paired samples |
| Turbidity | Moderate to good with local calibration | Estimate proxy; calibrate with sonde/turbidity meter and lab TSS |
| Total suspended solids (TSS) | Moderate to good in suitable water conditions | Empirical retrieval model validated against lab gravimetric TSS |
| Chlorophyll-a / algal bloom | Moderate to good under suitable conditions | Spectral proxy with local pigment samples |
| CDOM / coloured dissolved matter | Potentially useful | Model optical absorption; not a full dissolved-organics assay |
| Dissolved oxygen | Not directly measured by passive optical imagery | A multispectral model may correlate in a specific dataset, but use a sonde for measurement |
| Salinity / conductivity | Not directly measured reliably by ordinary optical imagery | Use conductivity/salinity sonde |
| Temperature | Not by standard visible/NIR multispectral sensor | Thermal camera can map surface temperature, not water-column profile |
| Dissolved arsenic, cadmium, chromium, copper, lead, zinc | Not directly identifiable at trace concentrations | Laboratory ICP-MS after water sampling |
| Total Hg / methylmercury | Not directly identifiable | Mercury-specific lab methods; DGT can add a labile-fraction measure |
| Dioxins/furans | Not directly identifiable | HRGC-HRMS on physical samples |
| PAHs / PCBs / VOCs | Not reliably identifiable as individual contaminants | Appropriate GC-MS/GC-MS/MS laboratory methods |
| PFAS | Not directly identifiable | Targeted laboratory methods if a source/pathway rationale exists |
| Submerged sediment chemistry | No | Sediment grabs/cores and laboratory analysis |
| Sediment thickness / bathymetry | Not reliably through opaque/turbid water | Sonar and cores; optical bathymetry only in shallow clear water with validation |
| Wetland vegetation stress | Good for mapping broad condition/change | Multispectral vegetation indices plus field ecology |
| Erosion / shoreline change | Good | Repeat orthomosaics and ground control |

## 4. Evidence from published drone-water-quality studies

- A 2024 review of UAV hyperspectral water-quality monitoring notes that calibration, atmospheric correction and modelling of non-water-colour parameters remain significant challenges.
- Giles et al. tested multispectral drones in a dynamic estuary using three field campaigns and multiple water-quality parameters. Eleven parameters had statistically significant correlations with image bands (R² > 0.4); the strongest reported correlation was chlorophyll with the green band (R² = 0.72). Crucially, the best predictor bands varied by month, and one model could not reproduce temporal variation in the dynamic estuary.
- Reviews of water-quality remote sensing emphasize the need for in-situ calibration/validation and limitations for optically inactive parameters.
- UAV hyperspectral systems are sensitive to radiometric calibration, sun glint, illumination changes, viewing geometry, sensor noise and spectral mixing. A reflectance panel alone may not remove all uncertainty.

This literature supports local proxy modelling, not chemical fingerprinting.

## 5. Boat Harbour-specific deployment concept

### Phase A — RGB and multispectral baseline

Use a repeatable drone platform with:
- high-quality RGB for orthomosaics and shoreline/vegetation documentation;
- multispectral bands appropriate to visible, red-edge and near-infrared observations;
- RTK/PPK or surveyed ground control for repeatable georeferencing;
- reflectance calibration and irradiance monitoring.

Map:
- shoreline and exposed sediment;
- wetland vegetation condition;
- erosion and deposition patterns;
- visible surface-water anomalies;
- repeatable changes after storms, seasonal shifts or project activity.

### Phase B — Paired water-quality retrieval

At selected image pixels/patches, collect same-time:
- turbidity;
- TSS;
- chlorophyll-a where relevant;
- CDOM where relevant;
- water depth, salinity, temperature, pH and dissolved oxygen;
- laboratory samples for target contaminants at selected stations.

Build local retrieval models only for parameters where the paired data show stable predictive value. Reserve independent samples for validation. Recalibrate seasonally if the model drifts.

### Phase C — Hyperspectral pilot

Only procure/rent hyperspectral equipment if Phase A/B demonstrates a decision that multispectral cannot support. Pilot on:
- known turbidity gradients;
- distinct water types/salinity zones;
- wetland vegetation;
- visible surface plume conditions;
- shallow clear-water bottom mapping where feasible.

Predefine the success criterion: improvement in prediction accuracy, anomaly discrimination or field-sampling efficiency sufficient to justify cost and processing complexity.

## 6. Sediment detection: what the drone cannot do

A surface optical sensor sees reflected light emerging from the water surface. Water attenuates light, and suspended particles and dissolved organic matter further alter the signal. In turbid estuarine water, bottom reflectance can be weak or absent. Even when shallow-water bathymetry can be estimated, that is not sediment chemistry.

Use:
- sonar for bathymetry and bottom morphology;
- sub-bottom profiling where suitable;
- sediment cores and grabs for thickness, stratigraphy and chemistry;
- laboratory analysis for contaminants.

## 7. Recommended sensor stack

| Instrument | Role | Does it identify contaminants? |
|---|---|---|
| RGB drone camera | Orthomosaics, shoreline, visible plume, erosion | No |
| Multispectral camera | Vegetation condition, optical water proxies | No direct chemical identification |
| Hyperspectral camera | Higher spectral resolution for locally calibrated optical proxies and vegetation discrimination | No direct broad contaminant assay |
| RTK/PPK GNSS | Georeferencing | No |
| Reflectance panel / irradiance sensor | Radiometric calibration | No |
| Multiparameter sonde | pH, temperature, conductivity, DO, turbidity, depth | Measures physical/chemical water parameters directly, not trace contaminant suite |
| Turbidity logger | Continuous turbidity trends | No chemical identity |
| DGT passive sampler | Labile/bioavailable metals at interface for supported analytes | Measures a defined labile fraction, not total inventory |
| Single/multibeam sonar | Bathymetry | No |
| Side-scan sonar | Bottom texture/targets | No |
| Sub-bottom profiler | Sediment layering/thickness where acoustic conditions allow | No chemical identity |
| Accredited laboratory | Specific contaminant identification and concentration | Yes |

## 8. Procurement rule

Do not buy a hyperspectral drone because a vendor claims “chemical detection.” Require:
1. named analyte and concentration range;
2. validated detection limit in natural water;
3. independent peer-reviewed validation in comparable water;
4. field calibration method and uncertainty;
5. false-positive/false-negative rates;
6. independent ground-truth results;
7. proof the system measures the chemical itself rather than a correlated proxy.

If a vendor cannot provide this, treat the claim as marketing and do not include it in the technical design.
