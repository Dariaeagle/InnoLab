# Elevation-Based Time-Series Snow and Glacier Analysis

This project provides an interactive tool built in **Google Earth Engine (GEE)** to analyze glacier and snow changes using multi-sensor satellite data and elevation-based binning.  
It enables users to explore temporal patterns of **NDSI**, **NDVI**, **NDWI**, and **Sentinel-1 backscatter** values across different elevation zones for any selected glacier or manually drawn region of interest (ROI).

---

## 🌍 Live Earth Engine App

**[Launch the Earth Engine App](https://code.earthengine.google.com/e22896c9346d3788282ba2363a5dd011)**

---

## Features

### 📌 ROI Selection
- Draw your own AOI directly on the map.
- Select glaciers from pre-loaded shapefiles:
  - Iceland  
  - Southern Andes  
  - Scandinavia  
  - Central Europe  

---

### 🗻 DEM Integration
- Automatically checks DEM coverage and clips to ROI.
- Supported DEMs:
  - **SRTM**
  - **COPERNICUS**
  - **Custom DEMs**

---

### 🌤️ Optical Data Filtering
- Supports datasets: **Landsat 5/7/8/9**, **Sentinel-2**, and **MODIS**
- Applies:
  - Cloud and snow masking
  - Scaling and band renaming
- Calculates:
  - **NDVI**
  - **NDWI**
  - **NDSI**

---

### 📆 Weekly Aggregation
- Weekly composite generation (median).
- Calculates mean index values **per elevation bin** (e.g., every 50 meters).

---

### 📡 Sentinel-1 Radar Analysis
- Full preprocessing pipeline:
  - Border noise correction
  - Terrain flattening
  - Multi-temporal speckle filtering
- Computes:
  - Mean backscatter per elevation bin and per date
- Supports:
  - **VH / VV** polarizations  
  - Orbit mode and relative orbit filtering

---

### 🧭 Aspect and Slope Masking (Optional)
- Filter DEM using slope and aspect:
  - Example: north-facing slopes with slope ≥ 5°
- Use masked DEM for focused analysis

---

### 📤 Export Results
- Export all results to **CSV**:
  - Elevation-bin statistics for each week
  - Ready for further processing (e.g., in Python)

---

## 📈 Further Visualization

Use the **`csv_processing.py`** script (included in this repository) for plotting time series and heatmaps from the exported CSVs.

---
