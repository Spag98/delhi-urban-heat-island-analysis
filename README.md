# Urban Heat Island & Vegetation Dynamics — Delhi

## Overview
This project analyzes the Urban Heat Island (UHI) effect in Delhi using multi-year Landsat 8 satellite data (2015–2024). It integrates remote sensing, GIS, and spatial statistics to examine how vegetation (NDVI) and land surface temperature (LST) interact over time.

---

## Objectives
- Analyze spatio-temporal variation in Land Surface Temperature (LST)
- Assess vegetation dynamics using NDVI
- Evaluate the relationship between NDVI and LST
- Identify spatial clustering patterns of urban heat

---

## Data Sources
- Landsat 8 imagery (2015, 2017, 2019, 2022, 2024)
- Delhi district boundary shapefile
- OpenStreetMap (for visual validation)

---

## Methodology

### 1. Preprocessing
- Cloud filtering and band selection
- Mosaicking for multi-tile years (2017, 2019)
- Clipping to Delhi boundary

### 2. Index Calculation
- NDVI derived from Red and Near-Infrared bands
- LST derived from Thermal Infrared band (ST_B10) with scaling

### 3. Zonal Statistics (QGIS)
- District-level aggregation of NDVI and LST
- Consolidation into a GeoPackage for multi-year analysis

### 4. Statistical Analysis (Python)
- Pearson correlation (NDVI vs LST)
- Temporal trend analysis
- Global Moran’s I (spatial autocorrelation)
- Getis–Ord Gi* (local hotspot analysis)

---

## Key Results
- Negative relationship observed between NDVI and LST across most years
- Correlation weakens by 2024, indicating influence of additional urban factors
- Weak spatial autocorrelation (Moran’s I ≈ 0.22, p ≈ 0.05)
- No statistically significant hotspots at district scale

---

## Outputs
- NDVI and LST maps (2024)
- NDVI vs LST scatter plots with regression
- Temporal trend charts
- Correlation analysis plots
- Spatial statistics results

---

## Tools & Technologies
- QGIS (raster processing, zonal statistics)
- Python (GeoPandas, Matplotlib, Seaborn)
- PySAL (libpysal, esda)
- Google Colab

---

## Key Insight
Vegetation contributes to localized cooling, but the weakening NDVI–LST relationship suggests that urban heat patterns are influenced by multiple factors beyond vegetation, including built-up density and surface characteristics.

---

## Future Work
- Higher-resolution (ward or pixel-level) analysis
- Land Use/Land Cover (LULC) integration
- Predictive modeling using machine learning

---

## Author
Shachi — Geospatial & Climate Data Analyst
