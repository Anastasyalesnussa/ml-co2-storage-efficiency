# CO₂ Storage Surrogate Modeling using SPE11C-A full 3D field-scale model.

### **Abstract**
Geological carbon storage is a key component of large-scale decarbonization strategies, yet high-fidelity reservoir simulations remain computationally expensive for predicting long-term CO₂ behavior in heterogeneous subsurface formations. This study develops a data-driven surrogate model for CO₂ injection and storage efficiency using the SPE Comparative Solution Project (CSP) 11C — a full 3D field-scale benchmark designed for multiphase CO₂ flow prediction. Leveraging high-resolution spatial fields and time-evolving mass-balance data, the workflow integrates physics-informed feature engineering with machine-learning architectures to approximate pressure evolution, plume migration, and storage performance at substantially reduced computational cost. Baseline regression models and neural networks are evaluated alongside advanced surrogate approaches, including 3D convolutional models and operator-learning frameworks. The results demonstrate the potential of data-driven surrogates to replicate key dynamical behaviors of CO₂ injection scenarios while providing rapid evaluation capabilities for site screening and sensitivity analysis. This work contributes a reproducible, scalable modeling framework that bridges numerical simulation and machine learning, supporting ongoing research efforts in carbon management, subsurface decarbonization, and energy-transition technologies.

---

## 1. Research Objectives
- Construct a clean, analysis-ready 4D dataset (x, y, z, t) from the SPE 11C spatial maps and time-series outputs.  
- Develop a surrogate model capable of predicting pressure evolution, CO₂ plume migration, mass distribution, and long-term storage efficiency.  
- Compare physics-based simulation behavior with machine-learning approximations.  
- Investigate how geology and injection conditions influence long-term containment.  
- Build a reproducible CCS-focused ML workflow suitable for academic research.

---

## 2. Dataset Overview: SPE CSP 11C (2023–2025)

### **2.1 Spatial Maps**
Each timestep snapshot includes:
- x, y, z coordinates  
- Pressure (Pa)  
- CO₂ saturation  
- CO₂ mass components (mobile, immobile, dissolved)  
- Water mass and densities  
- Gas/liquid densities  
- Temperature  

These represent the full 3D spatial distribution of CO₂-related properties.

### **2.2 Time Series**
Includes:
- Injection pressures (p1, p2)  
- Mass balance components (mobile, immobile, dissolved, sealed)  
- Boundary flux  
- Containment metrics  
- Time evolution of total CO₂ mass  

### **Why Version 11C?**
It provides a realistic 3D field-scale environment with geological layering, heterogeneity, and multiphase CO₂ behavior—ideal conditions for surrogate model development.

---

## 3. Methodology

### **3.1 Data Preparation**
- Convert large CSV files into efficient formats (Parquet/HDF5).  
- Remove inactive cells.  
- Normalize and align spatial maps with time-series data.  
- Reconstruct the 3D grid for each timestep.

### **3.2 Feature Engineering**
Physics-inspired features:
- Depth and structural zones  
- Distance to injection well  
- Saturation gradients  
- Pressure derivatives  
- CO₂ mass categories (mobile/immobile/dissolved)  
- Storage efficiency ratio  

### **3.3 Machine Learning Models**
Baseline models:
- RandomForestRegressor  
- XGBoostRegressor  
- Fully Connected Neural Network

Advanced surrogate models:
- 3D Convolutional Neural Network (3D-CNN)  
- 3D U-Net for spatial prediction  
- Fourier Neural Operator (FNO)  
- Physics-Informed Neural Networks (PINNs)  

Targets:
- Pressure distribution  
- CO₂ saturation  
- Storage efficiency  
- Mass evolution over time  

### **3.4 Evaluation Metrics**
- R²  
- RMSE  
- Spatial prediction error  
- Temporal accuracy  
- Plume evolution consistency  
- Comparison with SPE 11C physical simulation

---

## 4. Tools & Libaries
- Python  
- NumPy, Pandas, SciPy  
- Scikit-learn, XGBoost  
- TensorFlow / PyTorch  
- PyVista, Plotly  
- dask, pyarrow  

---

## 5. Expected Results
- Machine-learning-predicted 3D CO₂ plume evolution  
- Surrogate pressure buildup curves  
- Storage efficiency prediction vs. SPE 11C reference  
- Sensitivity analysis for geological risk zones  
- Visual comparison of ML and simulation-based outputs  
  
---

## 🔬 6. Future Work
- Integrate MRST-based simulations for expanded parameter space.  
- Extend surrogate model to multi-scenario injection optimization.  
- Apply transfer learning using real CCS datasets (e.g., Sleipner).  
- Develop a publication-ready open-source CCS surrogate benchmark.  
   
---

## Repository Structure
```
ccs_11c_surrogate_model/
│
├── data/
│ ├── raw/
│ ├── interim/
│ └── processed/
│
├── notebooks/
│ ├── 1_Data_Exploration.ipynb
│ ├── 2_Preprocessing.ipynb
│ ├── 3_Feature_Engineering.ipynb
│ ├── 4_ML_Baseline_Models.ipynb
│ ├── 5_Surrogate_3D_Model.ipynb
│ └── 6_Visualization_Results.ipynb
│
├── src/
│ ├── data/
│ ├── features/
│ ├── models/
│ └── visualization/
│
├── models/
│ ├── baseline.pkl
│ └── surrogate_unet.pth
│
├── reports/
│ ├── figures/
│ └── manuscript/
│
├── environment.yml
└── README.md
```
---

## Author
**Anastasya Lesnussa**
Petroleum Engineer | Data Science for Energy Transition  
Portfolio: [yourwebsite.com] (replace later when ready)

---
### Keywords
`CO2 Storage`, `Machine Learning`, `Energy Transition`, `Surrogate Modeling`, `Reservoir Simulation`, `Decarbonization`
