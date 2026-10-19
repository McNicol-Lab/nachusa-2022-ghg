# Nachusa Grasslands Field Study 2022

Greenhouse gas flux data and ancillary in-situ environmental measurements for Nachusa Grasslands research in 2022.

## About

Analysis of chamber-based CO₂, CH₄, and N₂O fluxes collected across prairie, woodland, and wetland cover types at Nachusa Grasslands in 2022. Includes quality control, summary statistics, site-effect testing, relationships with soil temperature and moisture, decision-tree modeling, Q₁₀ estimation, and comparison to prior work. Prepared for the *Frontiers in Environmental Science* special issue.

## Key processing steps (in `flux-analysis.Rmd`)

1. **Data import and wrangling** — Load full flux dataset, recode ecosystems into cover types (prairie, woodland, wetland) and site numbers, and join site coordinates.
2. **Flux QA/QC** — Flag bad injections (high CO₂ *p*-value or extreme woodland CO₂), set affected fluxes to NA, and set non-significant CH₄/N₂O slopes to zero.
3. **Summary and visualization** — Density plots, summary statistics (min, quartiles, max), and soil temperature/moisture patterns by cover and date.
4. **Statistical analysis** — Linear models testing site effects within cover; decision trees (`rpart`) for flux responses to soil temperature, moisture, and cover; Q₁₀ calculation for CO₂.
5. **External comparison and meteorology** — Summarize Koyama et al. CH₄ data and local temperature/precipitation records.

## Repository structure

- `data/` — Raw and compiled flux, ancillary, and meteorological datasets  
- `code/` — Supporting scripts by year  
- `paper-figures/` — Figures prepared for the manuscript  
- `plots/` — Additional visualizations  
- `map manual/` — Mapping materials  
- `2022-nachusa-fluxes.csv` — Final tidy flux dataset with coordinates  
- `2022-site-coords.csv` — Site coordinates  
- `flux-analysis.Rmd` — Main analysis notebook  
- `site-coords.Rmd` — Coordinate handling  
- `figure-1-map.png` — Study-site map  

## Key outputs

- Cleaned 2022 flux dataset with cover, site, and coordinate information  
- Summary statistics and density plots by gas and cover  
- Linear-model and decision-tree results relating fluxes to soil conditions  
- Q₁₀ estimates and soil temperature/moisture summaries  
- Paper-ready figures  

## Notes

Fluxes are reported in µmol m⁻² s⁻¹ (CO₂) and nmol m⁻² s⁻¹ (CH₄, N₂O). Detection limits were calculated from instrument precision and chamber geometry.
