# Machine learning Prediction of CO2 Storage Efficiency

This project applies **machine learning and data-driven modeling** to evaluate the **efficiency and performance of CO2 geological storage**. It uses the **SPE10 synthetic reservoir dataset** and later integrates **Sleipner CO2 injection field data** to develop a **surrogate model** for predicting CO2 distribution and injection efficiency - supporting **energy transition and decarbonization** research.

## Project Goals
- Build a **data-driven surrogate model** for CO2 storage simulation.
- Predict **CO2 plume behaviour**. **storage efficiency**, and **risk indicators** using ML techniques.
- Bridge **reservoir simulation data** with **machine learning frameworks** to reduce computational cost.
- Contribute to the field of **data science for decarbonization and carbon management**.

## Dataset
### 1. SPE10 Synthetic Model
- **Files:** `spe_phi.dat` (porosity) and `spe_perm.dat` (permeabilty)
- **Grid size:** 60 x 220 x 85
- **Variables:**
  - Porosity field (ϕ)
  - Permeabilty tensor (Kx, Ky, Kz)
- Source: [SPE Comparative Solution Project](https://www.spe.org/web/csp/datasets/set02.htm)

### 2. Sleipner CO2 Storage (to be added)
- Real field CO2 injection time series (pressure, plume extent, seismic depth maps)
- Source: [Sleipner Benchmark Dataset - SINTEF / IEAGHG](https://co2datashare.org)

---

## Workflow
1. **Data Processing**
   - Load porosity & permeability fields
   - Normalize and visualize 3D grid structure
   - Generate synthetic injection scenarios

2. **Simulation Proxy**
   - Compute CO2 saturation fronts (syntethic)
   - Label training data for ML training
  
3. **Machine Learning Model**
   - Test algorithms: `RandomForestRegressor`, `XGBoost`, `3D CNN`
   - Predict CO2 saturation / efficiency metrics
   - Evaluate R², RMSE, and uncertainty bounds
  
  4. **Risk Assessment**
     - Sensitivity analysis for reservoir heterogeneity
     - Identify hugh-leakage or low-efficiency regions
    
---

## Tools & Libaries
- Python, NumPy, Pandas, Matplotlib
- Scikit-learn, XGBoost, TensorFlow / PyTorch
- PyVista or Plotly (for 3D visualization)
- (Optional) SciPy or `pytorch-lightning` for experiments

---

## Expected Outputs
- 3D visualization of CO2 plume prediction
- Comparison of ML-predicted vs simulated efficiency
- Sensitivity and uncertainity plots
- Summary report for model validation

---

## Next Steps
- Integrate **Sleipner field data** for transfer learning.
- Publish results as a **data-driven CCS research notebook**.
- Extend framework to **multi-well CO2 injection optimization**.

---
## Author
**Anastasya Lesnussa**
Petroleum Engineer | Data Science for Energy Transition  
Portfolio: [yourwebsite.com] (replace later when ready)

---
### Keywords
`CO2 Storage`, `Machine Learning`, `Energy Transition`, `Surrogate Modeling`, `Reservoir Simulation`, `Decarbonization`
