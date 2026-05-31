# Flood-Risk-Assessment-project-of-Sylhet-Division
A GIS-based flood risk assessment of Bangladesh's Sylhet Division using ArcGIS Pro. By weighting elevation, slope, drainage density, LULC, river proximity, and 5-year rainfall data (2018–2023), this project models spatial vulnerability across critical haor basins like Sunamganj to back data-driven disaster management.
# Spatial Flood Risk Assessment & Hydrological Vulnerability Analysis: Sylhet Division, Bangladesh

A data-driven spatial engineering project utilizing **ArcGIS Pro** and Multi-Criteria Decision Analysis (MCDA) via the Analytical Hierarchy Process (AHP) to evaluate regional flood susceptibility, hazard zones, and socio-environmental risk profiles across the Sylhet Division.

---

## ⚙️ Analytical Framework & Core Factors
To accurately map terrain weaknesses and drainage inefficiencies, this model integrates six distinct biophysical and hydro-meteorological raster variables:

### 1. Elevation Mapping
Derived from SRTM DEM data to isolate low-lying catchments acting as natural sinks.
![Elevation Mapping](Elevation(%20Sylhet%20Division).jpg)

### 2. Slope Geometry
Slope gradients calculated in degrees to evaluate surface velocity and velocity retention characteristics.
![Slope Analysis](Slope%20Analysis(Sylhet%20Division).jpg)

### 3. Drainage Density
Derived using D8 flow direction arrays and stream accumulation metrics to quantify localized hydraulic evacuation efficiency.
![Drainage Density](Drainage%20Density(Sylhet%20Division).jpg)

### 4. Land Use / Land Cover (LULC)
Supervised classification of Landsat 8 bands to evaluate surface roughness and infiltration/runoff coefficients.
![Land Use Land Cover](Land%20Use%20Land%20Cover(%20Sylhet%20Division).jpg)

### 5. Proximity to Fluvial Networks
Buffer-proximity analytics measuring spatial exposure to the Surma and Kushiyara main river channels.
![River Proximity Analysis](River%20Proximity%20Analysis(Sylhet%20Division).jpg)

### 6. Precipitation Intensity
CHIRPS Gridded Rainfall variations across a 5-year spatial-temporal baseline (2018–2023).
![Average Rainfall](Average%20Rainfall(Sylhet%20Division).jpg)

---

## 📊 Final Integrated Model
The final integrated model weights and overlays all components to classify regional flood risk into 5 distinct intervals—from Very Low to Very High risk.

![Flood Risk Assessment](Flood%20Risk%20Assessment(Sylhet%20Division).jpg)
