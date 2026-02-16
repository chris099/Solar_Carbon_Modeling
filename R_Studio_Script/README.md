# Utility-Scale Solar Carbon Impact Assessment (Massachusetts)

This repository contains code and workflows for quantifying the carbon impacts of utility-scale solar development in Massachusetts.

The analysis integrates:

- Land-cover change detection (remote sensing)
- Terrestrial carbon bookkeeping
- Life-cycle assessment (LCA) of solar PV
- Grid carbon intensity scenarios
- Monte Carlo uncertainty propagation

The framework estimates:

1. Deforestation-related emissions  
2. Loss of potential sequestration (LoPS)  
3. Solar life-cycle emissions (installation + end-of-life)  
4. Avoided emissions from displaced grid electricity  
5. Net carbon impact over 2005–2054  


---

## Core Modeling Components

| Component | Description |
|------------|------------|
| Carbon Bookkeeping | Biomass stock loss + decay dynamics |
| LoPS | Lost future sequestration after deforestation |
| LCA | PV learning-curve–based carbon intensity |
| Avoided Emissions | ISO-NE grid carbon intensity scenario |
| Monte Carlo | Uncertainty propagation (area, biomass, decay, LCA, generation) |

---

## Time Period

- Historical inputs: 2005–2024  
- Results timeline: 2005–2054  
- PV lifetime: 30 years  

---

## Output

The model produces:

- Annual fluxes (MgC yr⁻¹)
- Cumulative emissions
- 95% confidence intervals
- Component-level breakdown plots
- Net carbon impact trajectories

---

## Citation

This repository contains code developed as part of Kangjoon Cho’s Ph.D. dissertation at Boston University.

Associated publications and dissertation citation details will be provided upon formal publication.

For citation inquiries, please contact the author.

---

## Contact

For questions regarding methodology or modeling framework, please contact: kangjoon@bu.edu

Kangjoon Cho  
Boston University – Department of Earth & Environment
