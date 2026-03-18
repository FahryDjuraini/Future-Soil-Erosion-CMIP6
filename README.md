# 🌍 Climate Change Impacts on Soil Erosion in a Tropical Watershed
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19089923.svg)](https://doi.org/10.5281/zenodo.19089923)

This repository provides a complete and reproducible workflow for assessing soil erosion dynamics under climate change scenarios in a tropical watershed. The framework integrates **Regional Climate Model outputs (SINGV)**, **Google Earth Engine (GEE)**, and the **Revised Universal Soil Loss Equation (RUSLE)**.

---

## 📖 Overview

Soil erosion is a major environmental challenge in tropical regions, particularly under changing climate conditions. This study quantifies historical and future soil erosion using a multi-source, multi-method approach combining:

- 🌧️ Climate projections (RCM - SINGV)
- 🛰️ Remote sensing data (Google Earth Engine)
- 🌱 RUSLE model (R, K, LS, C, P factors)
- 📊 Statistical evaluation and bias correction

---

## 📦 Repository Structure

### 1. RUSLE Factor Calculation (GEE)
- Computes:
  - Soil erodibility (K)
  - Rainfall erosivity (R)
  - Slope length & steepness (LS)
- Data sources:
  - SoilGrids
  - CHIRPS
  - MERIT Hydro
  - HiHydroSoil

---

### 2. Soil Erosion Modeling (GEE)
Implements full RUSLE model:

A = R × K × LS × C × P

Outputs:
- Baseline (2024)
- Future scenarios:
  - SSP245 (2040, 2060)
  - SSP585 (2040, 2060)

Includes erosion classification based on Indonesian standards.

---

### 3. Bias Correction & Model Evaluation (Python)
- Hybrid Quantile Mapping (QM)
- Multi-Model Ensemble (MME):
  - Mean
  - Median
- Evaluation metrics:
  - Correlation
  - RMSE
  - PBIAS
  - KGE
- Visualization:
  - Taylor Diagram

---

### 4. Historical Analysis (Python)
- Visualization of:
  - R, K, LS, C, P factors
  - Historical soil loss
- Statistical analysis:
  - Mean, median, min, max, std

---

### 5. Future Soil Erosion Analysis (Python)
- Scenario-based spatial analysis
- National erosion classification
- Area calculation (ha & %)
- Dominant class identification

---

### 6. Delta Erosion Analysis (Python)
- Change detection (Future - Baseline)
- Outputs:
  - Increase / decrease / stable zones
  - Area statistics
  - Diverging maps

---

## 🔬 Key Features

- 🌐 Fully reproducible workflow (GEE + Python)
- 📊 Multi-scenario climate analysis (SSP245 & SSP585)
- 🧠 Advanced bias correction (Hybrid Quantile Mapping)
- 📈 Robust evaluation (Taylor Diagram + statistical metrics)
- 🗺️ High-resolution spatial analysis (30 m)
- 📉 Change detection for impact assessment

---

## 🎯 Study Context

This repository supports the research:

**"Climate Change Impacts on Soil Erosion in a Tropical Watershed: Insights from SINGV Regional Climate Modeling and RUSLE"**

Objectives:
- Quantify climate change impacts on soil erosion
- Evaluate future erosion risks
- Support sustainable watershed management

## 📂 Data Availability

All datasets used in this study are publicly available on Zenodo:

🔗 https://doi.org/10.5281/zenodo.19089923

The dataset includes:
- Climate model outputs (SINGV RCM)
- Processed rainfall data
- RUSLE factor inputs
- Soil erosion outputs (historical and future scenarios)

Due to size limitations, datasets are not stored in this repository. Users are encouraged to download the data directly from Zenodo and use it with the provided scripts.

---

## 🛠️ Requirements

### Google Earth Engine
- JavaScript API

### Python (≥ 3.9)
Required libraries:



---

## 🚀 How to Use

1. Download dataset from Zenodo:
   https://doi.org/10.5281/zenodo.19089923

2. Run GEE scripts to generate:
   - R, K, LS, C, P factors
   - Soil loss maps

3. Export results to GeoTIFF

4. Use Python scripts to:
   - Perform bias correction
   - Analyze historical & future erosion
   - Generate figures and statistics

---

## 📌 Notes

- Scripts are modular and adaptable to other watersheds
- Input data (AOI, climate scenarios) should be customized
- Outputs are suitable for:
  - Scientific publication
  - Policy and planning support

---

## 👨‍💻 Author

Djuraini, M. F., Utami, S., Adzimah, N. L., Benediktus, S., Mellyana, I. M., Putri, N. R. C., Hidayat, W., & Mulabbi, A. (2026).

How to cite :

Djuraini, M. F., Utami, S., Adzimah, N. L., Benediktus, S., Mellyana, I. M., Putri, N. R. C., Hidayat, W., & Mulabbi, A. (2026). Climate Change Impacts on Soil Erosion in a Tropical Watershed: Insights from SINGV Regional Climate Modeling and RUSLE [Data set]. Zenodo. https://doi.org/10.5281/zenodo.19089923

---

## 📬 Contact

📧 mohfahrydjuraini@mail.ugm.ac.id

---
