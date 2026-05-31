# Flood-Risk-Assessment-project-of-Sylhet-Division
A GIS-based flood risk assessment of Bangladesh's Sylhet Division using ArcGIS Pro. By weighting elevation, slope, drainage density, LULC, river proximity, and 5-year rainfall data (2018–2023), this project models spatial vulnerability across critical haor basins like Sunamganj to back data-driven disaster management.
# Spatial Flood Risk Assessment & Hydrological Vulnerability Analysis: Sylhet Division, Bangladesh

A data-driven spatial engineering project utilizing **ArcGIS Pro** and Multi-Criteria Decision Analysis (MCDA) via the Analytical Hierarchy Process (AHP) to evaluate regional flood susceptibility, hazard zones, and socio-environmental risk profiles across the Sylhet Division.

---

## ⚙️ Analytical Framework & Core Factors
To accurately map terrain weaknesses and drainage inefficiencies, this model integrates six distinct biophysical and hydro-meteorological raster variables:

*   **Elevation Mapping:** Derived from SRTM DEM data to isolate low-lying catchments acting as natural sinks. 
    *   *Reference Layer:* `Elevation( Sylhet Division).jpg`
*   **Slope Geometry:** Slope gradients calculated in degrees to evaluate surface velocity and velocity retention characteristics.
    *   *Reference Layer:* `Slope Analysis(Sylhet Division).jpg`
*   **Drainage Density:** Derived using D8 flow direction arrays and stream accumulation metrics to quantify localized hydraulic evacuation efficiency.
    *   *Reference Layer:* `Drainage Density(Sylhet Division).jpg`
*   **Land Use / Land Cover (LULC):** Supervised classification of Landsat 8 bands to evaluate surface roughness and infiltration/runoff coefficients.
    *   *Reference Layer:* `Land Use Land Cover( Sylhet Division).jpg`
*   **Proximity to Fluvial Networks:** Buffer-proximity analytics measuring spatial exposure to the Surma and Kushiyara main river channels.
    *   *Reference Layer:* `River Proximity Analysis(Sylhet Division).jpg`
*   **Precipitation Intensity:** CHIRPS Gridded Rainfall variations across a 5-year spatial-temporal baseline (2018–2023).
    *   *Reference Layer:* `Average Rainfall(Sylhet Division).jpg`

---

## 📊 Engineering Insights & Key Findings
The final integrated model classifies regional flood risk into 5 distinct intervals—from Very Low to Very High risk.
*   *Reference Layer:* `Flood Risk Assessment(Sylhet Division).jpg`
