# Main Carbon Modeling Framework

This directory contains the integrated carbon impact model for utility-scale solar development in Massachusetts.

The model combines:

- Carbon bookkeeping (deforestation + decay)
- Loss of potential sequestration (LoPS)
- Solar PV life-cycle emissions
- Avoided grid emissions
- Monte Carlo uncertainty propagation

---

## Model Components

### 1. Carbon Bookkeeping

- Baseline biomass from 2016 Treemap
- Growth rate estimated from FIA data
- Partitioning:
  - 50% immediate emissions (burn)
  - 25% softwood decay
  - 25% hardwood decay
- First-order decay functions

---

### 2. Loss of Potential Sequestration (LoPS)

LoPS is calculated as: 
LOPS_y = Growth_rate × Cumulative_deforested_area
Units: MgC yr⁻¹

---

### 3. Solar LCA

- PV carbon intensity derived from learning curve regression
- Installation-year carbon intensity applied
- Lifetime electricity generation from SAM
- End-of-life credits included

---

### 4. Avoided Emissions

- Grid carbon intensity: ISO-NE annual average
- Applied from installation year forward
- 30-year project lifetime

---

## Monte Carlo Simulation

Uncertainties included:

- Total deforestation area
- Biomass density
- Biomass growth rate
- Decay constants
- Solar generation variability
- LCA intensity
- Grid carbon intensity

Typical configuration: n_iter = 5000


Outputs include:

- Annual mean flux
- 95% CI
- Cumulative emissions
- Component breakdown

---

## Outputs Generated

- Stacked emissions plots
- Net carbon trajectory
- Component-wise uncertainty bands
- Cumulative carbon balance

---

## Time Period

- Historical: 2005–2024
- Projection: 2025–2054
- Total simulation window: 50 years

