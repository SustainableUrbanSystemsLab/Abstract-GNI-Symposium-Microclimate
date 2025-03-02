# A Comparative Study on the Urban Weather Generator: How Useful Is It for Urban Decision-Making?

<img src="https://raw.githubusercontent.com/SustainableUrbanSystemsLab/Abstract-GNI-Symposium-Microclimate/main/Figures/georgia_tech_map_with_tiles.png" width="350px"><img src="https://raw.githubusercontent.com/SustainableUrbanSystemsLab/Abstract-GNI-Symposium-Microclimate/main/Figures/Diurnal_Hottest_Month_July.png" width="372px">

## Abstract
Microclimates are localized regions in which environmental conditions differ from those of the surrounding areas. As urban areas grow, sustainable urban planning and microclimate management become increasingly important. The Urban Weather Generator (UWG) addresses some challenges by estimating hourly canopy and air temperatures with minimal computational overhead and only cursory building geometry inputs.

This study focuses on evaluating UWG’s usefulness for campus-scale decision-making, using Georgia Tech as a testbed. A variance-based sensitivity analysis reveals the parameters most influential to UWG outputs, highlighting that even seemingly minor parameters can be significant when combined. Finally, we compare actual campus weather data from Georgia Tech’s CRC station to UWG’s output to illustrate real-world performance.

## Authors
- **Ze Yu Jiang**  
- **Sofia Mujica**  
- **Maryam Almaian**  
- **Patrick Kastner** (Corresponding Author)  
  [patrick.kastner@gatech.edu](mailto:patrick.kastner@gatech.edu)

## Introduction
Urban campuses like Georgia Tech are rapidly expanding while aiming to mitigate urban heat islands. Tools to quickly assess campus-scale temperature changes are essential for robust planning. The Urban Weather Generator (UWG) adjusts a standard EnergyPlus Weather (EPW) file based on building density, vegetation coverage, and other local boundary conditions, outputting a microclimate-adjusted EPW.

## Methods
1. **Data Collection and Pre-processing**  
   - Hourly and sub-hourly weather data were gathered from the KGAATLAN216 (CRC) station, then resampled to hourly intervals.
   - Key morphological inputs included building density, tree coverage, and grass coverage, each determined from the campus maps.

2. **Sobol Sensitivity Analysis**  
   - 14 UWG parameters were examined for their influence on the difference between the reference EPW temperatures and UWG-adjusted temperatures.
   - A high number (100,000) of samples were run, measuring both first-order (individual) and total-order (cumulative) impact.

3. **Scenario Testing**  
   - A proposed campus extension, Science Square, was simulated to see how temperature profiles might shift compared to existing campus conditions.
   - Building density, tree cover, and grass cover were varied to gauge their impact on peak daytime temperatures.

## Results
- **Sensitivity**  
  Wind minimum speed, vertical-to-horizontal ratio, and daytime urban boundary layer height emerged as key parameters, though interaction effects show that seemingly minor parameters can still significantly affect UWG outputs in combination.
- **UWG vs. Observations**  
  Differences of 0.1–0.3°C appeared in the early afternoon for some scenarios, with negligible differences at night. UWG thus provides a quick, approximate forecasting method for campus-scale microclimates.

## Discussion & Conclusion
UWG’s relatively small data requirements and low computational overhead make it appealing for urban planners and campus decision-makers. However, uniform parameter assumptions (such as wind velocity) and the overlap constraints on grass, tree, and building coverage limit the resolution of results. Future work includes finer tiling of campus areas to better represent local variations.

## Repository Structure


- `Code` - [Here](https://github.com/SustainableUrbanSystemsLab/CP-GNI2024-UWG)
- `Figures` - (Campus maps, radial plots, sensitivity index images, etc.)  
- `bib.bib`  - (BibTeX references for citations)  
- `main.tex`  - (LaTeX source for the complete paper)  
- `main.pdf`  - (Compiled PDF version of the paper)  
- `README.md`  - this document


## Keywords
`Urban Weather Generator, UWG, Microclimates, Sensitivity Analysis, Georgia Tech, Urban Planning, EPW`

## Citation
If you wish to cite this work, you can use a format similar to:
```bibtex
@inproceedings{jiang2024UWG,
  title     = {A Comparative Study on the Urban Weather Generator: How Useful Is It for Urban Decision-Making?},
  author    = {Jiang, Ze Yu and Mujica, Sofia and Almaian, Maryam and Kastner, Patrick},
  booktitle = {GNI Symposium \& Expo on Artificial Intelligence for the Built World},
  year      = {2024},
  address   = {Technical University of Munich}
}
```

---

[Link to this repository](https://github.com/SustainableUrbanSystemsLab/Abstract-GNI-Symposium-Microclimate)
