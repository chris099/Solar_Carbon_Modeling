# Pre-processing and Input Parameter Estimation

This directory contains scripts used to generate model inputs for the main carbon modeling framework.

Pre-processing outputs are required before running: MainCarbonModel/006. CarbonBookkeeping+MonteCarlo.rmd

---

## 1. Annual Biomass Growth (FIA)

File: rFIA_app.Rmd

Purpose:
- Retrieve Massachusetts FIA plot data
- Estimate annual biomass carbon density
- Fit growth model (linear and logarithmic)
- Perform parametric bootstrap
- Export bootstrap slope draws

Output: boot_growth2.rds


---

## 2. Treemap 2016 Biomass Bootstrap

File: Boot_Biomass.Rmd

Purpose:
- Use Treemap histogram of biomass density
- Convert to MgC/ha
- Multinomial bootstrap sampling
- Estimate biomass uncertainty for solar footprint

Output: boot_biomass16.rds


---

## 3. Electricity Generation (SAM)

File: Electricity Generation (SAM).Rmd

Purpose:
- Import SAM simulation results
- Stratify by EPA Level-III ecoregions
- Apply area-weighted averaging
- Bootstrap annual generation

Output: sam_generation_bootstrap.rds

---

## 4. PV Learning Curve (LCA)

File: LCA_Solar_LearningCurve.Rmd

Purpose:
- Compile historical PV LCA estimates
- Merge with global cumulative installed capacity
- Fit log-log learning curve model
- Estimate annual PV carbon intensity (2005–2024)

Output: pv_ci_0524.rds

---

## 5. Grid Carbon Intensity

File: GRID_Carbon Intensity.Rmd

Purpose:
- Import ISO-NE annual carbon intensity
- Convert lbs/MWh → gCO₂/kWh
- Prepare scenario input for avoided emissions

Output: ISO_NE_CI.rds
