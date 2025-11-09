# Raw Data - CO₂ Storage Modeling

This folder contains (or references) the raw input data used to develop the **machine learning prediction model for CO₂ storage efficiency**.

Because the original dataset is too large for GitHub’s file size limits, it is **hosted externally**. You can download it from the official or processed sources listed below.

---

## 🧱 1. SPE10 Synthetic Reservoir Model

**Description:**  
A benchmark geological model representing part of the Brent sequence (Tarbert & Upper Ness formations).  
Used to generate synthetic porosity and permeability fields for surrogate model training.

- **Porosity file:** `spe_phi.dat`  
- **Permeability file:** `spe_perm.dat`  
  - Dimensions: 60 × 220 × 85  
  - Variables: `Kx`, `Ky`, `Kz`

**Original Source:**  
[SPE Comparative Solution Project – Model 2](https://www.spe.org/web/csp/datasets/set02.htm)

**Download (processed version):**  
[Google Drive link — Anastasya Lesnussa (SPE10 porosity and permeability )](https://drive.google.com/drive/folders/1GVsxah8SBwNPVMuEkUT_HyJaCqG6XUBJ?usp=sharing)  

---

## 🌍 2. Sleipner CO₂ Storage Dataset (Planned)

The **Sleipner field** dataset will be used later for model validation and transfer learning.  
It includes time-series injection and seismic data for CO₂ plume evolution.

**Source:** [CO₂ DataShare – Sleipner Dataset](https://co2datashare.org/dataset/sleipner)

---

## 🧠 Notes

- Files should be placed locally in this directory after download:  

data/raw/spe_phi.dat
data/raw/spe_perm.dat

