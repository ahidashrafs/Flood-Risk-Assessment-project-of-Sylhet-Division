# Flood-Risk-Assessment-project-of-Sylhet-Division
A GIS-based flood risk assessment of Bangladesh's Sylhet Division using ArcGIS Pro. By weighting elevation, slope, drainage density, LULC, river proximity, and 5-year rainfall data (2018–2023), this project models spatial vulnerability across critical haor basins like Sunamganj to back data-driven disaster management.
# Spatial Flood Risk Assessment & Hydrological Vulnerability Analysis: Sylhet Division, Bangladesh

A data-driven spatial engineering project utilizing **ArcGIS Pro** and Multi-Criteria Decision Analysis (MCDA) via the Analytical Hierarchy Process (AHP) to evaluate regional flood susceptibility, hazard zones, and socio-environmental risk profiles across the Sylhet Division.

---

##  Analytical Framework & AHP Multi-Criteria Weighting
To remove subjectivity from the spatial overlay, an Analytical Hierarchy Process (AHP) pair-wise comparison matrix was established. The table below details the target layer allocations, calculated influence percentages, and the underlying engineering justification used in the ArcGIS Pro `Weighted Sum` pipeline.

| Spatial Variable | AHP Weight (%) | Hydraulic Layer Role | Engineering Justification |
| :--- | :--- | :--- | :--- |
| **Elevation (DEM)** | 30% | Primary Sink Identifier | Governs gravitational water pooling; low-lying basins serve as regional collection sinks. |
| **Average Rainfall** | 20% | Hydro-Meteorological Hazard | Defines the volumetric input boundary condition across a 5-year baseline (2018–2023). |
| **Slope Analysis** | 15% | Surface Runoff Velocity | Dictates time-of-concentration; flat terrains stall drainage, steep zones accelerate runoff. |
| **River Proximity** | 15% | Fluvial Exposure Buffer | Determines high-risk zones vulnerable to immediate out-of-bank channel spilling. |
| **Drainage Density** | 10% | Network Evacuation Capacity | Quantifies structural efficiency of the localized channel matrix to discharge excess water. |
| **Land Use / Cover** | 10% | Surface Roughness / Infiltration | Regulates the runoff coefficient ($C$) based on soil infiltration and impervious areas. |

---

##  Risk Factor
The raster reclassification table below maps how physical ground characteristics step-wise translate into localized flood vulnerability indices (Scaled from 1 = Very Low to 5 = Very High) during spatial normalization:

| Index Value | Vulnerability Class | Topographical Profiles | Land Cover Type (LULC) | Hydrological Exposure |
| :---: | :--- | :--- | :--- | :--- |
| **1** | **Very Low** | High Elevation, Steep Slopes | Dense Forest Canopies | Low Precipitation, Far from Rivers |
| **2** | **Low** | Elevated/Moderate Slopes | Planted / Cultivated Land | Medium Rainfall Zone |
| **3** | **Moderate** | Rolling Terrain, Low Basins | Developed / Built-up Areas | Standard Buffer Drainage Density |
| **4** | **High** | Gentle Slopes, Low Plains | Bare Soil / Exposed Land | High Cumulative Rainfall Intensity |
| **5** | **Very High** | Depression Basins (Haors) | Open Water Bodies | Immediate Banks / Low Drainage Density. |

---

## ⚙️ Core Factors & Spatial Input Graphics

### 1. Elevation Mapping
Derived from SRTM DEM data to isolate low-lying catchments acting as natural sinks.
![Elevation Mapping](Elevation(%20Sylhet%20Division).jpg)

### 2. Slope Analysis
Slope gradients calculated in degrees to evaluate surface velocity and velocity retention characteristics.
![Slope Analysis](Slope%20Analysis(Sylhet%20Division).jpg)

### 3. Drainage Density
Derived using D8 flow direction arrays and stream accumulation metrics to quantify localized hydraulic evacuation efficiency.
![Drainage Density](Drainage%20Density(Sylhet%20Division).jpg)

### 4. Land Use / Land Cover (LULC)
Supervised classification of Landsat 8 bands to evaluate surface roughness and infiltration/runoff coefficients.
![Land Use Land Cover](Land%20Use%20Land%20Cover(%20Sylhet%20Division).jpg)

### 5. Proximity to River
Buffer-proximity analytics measuring spatial exposure to the Surma and Kushiyara main river channels.
![River Proximity Analysis](River%20Proximity%20Analysis(Sylhet%20Division).jpg)

### 6. Precipitation Intensity
CHIRPS Gridded Rainfall variations across a 5-year spatial-temporal baseline (2018–2023).
![Average Rainfall](Average%20Rainfall(Sylhet%20Division).jpg)

---

##  Final Model
The final integrated model weights and overlays all components to classify regional flood risk into 5 distinct intervals—from Very Low to Very High risk.

![Flood Risk Assessment](Flood%20Risk%20Assessment(Sylhet%20Division).jpg)

💡Key Insight:
The model isolates Sunamganj District as a critical high-vulnerability hotspot. This is hydrologically justified by its flat terrain profiles (<2° slopes), low drainage density capacity, and direct exposure to transboundary monsoonal rainfall channels coupled with out-of-bank flow from the Surma and Kushiyara rivers. Conversely, Moulvibazar District demonstrates high systemic resilience due to higher elevation barriers and forest canopies that naturally attenuate peak runoff curves.


---

## 🛠️ Geoprocessing & Spatial Toolsets Used
* **Hydrology Extension:** `Fill`, `Flow Direction (D8)`, `Flow Accumulation`, `Stream Link`
* **Surface & Distance Analysis:** `Slope`, `Euclidean Distance`
* **Map Algebra Engine:** Spatial reclassification and weighted linear combinations (`Weighted Sum`) to execute the AHP vulnerability matrix.

---

## 📂 Source Data Provenance
* **Digital Elevation Model & Landsat 8 Data:** [USGS EarthExplorer](https://earthexplorer.usgs.gov/)
* **Spatio-Temporal Rainfall Data:** [CHIRPS / Climate Hazards Center](https://www.chc.ucsb.edu/data/chirps)
