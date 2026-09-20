# Hurricane Wind Value-at-Risk from an AI Weather Ensemble

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Climate Risk](https://img.shields.io/badge/Climate%20Risk-Catastrophe%20Modeling-2E8B57)](https://www.climatechange.ai/)
[![Geospatial](https://img.shields.io/badge/Analysis-Geospatial-4C8CBF)](https://geopandas.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An end-to-end catastrophe-risk workflow that converts a 50-member AI hurricane forecast ensemble into county-level **wind-damage Value-at-Risk (VaR)** estimates for single-family homes in Florida, Georgia, South Carolina, and North Carolina.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lonfea/hurricane-wind-var/blob/main/Hurricane_Wind_VaR.ipynb)

## Why this project matters

Insurers, mortgage holders, governments, and coastal investors need quantified estimates of potential storm losses before landfall. A single deterministic forecast hides important uncertainty. Ensemble forecasts instead produce a distribution of plausible outcomes, allowing decision-makers to evaluate tail risk rather than relying on one scenario.

## Modeling chain

```text
AI forecast ensemble → wind hazard → property exposure → vulnerability → loss distribution → Value-at-Risk
```

The analysis uses Google's experimental WeatherNext cyclone ensemble for the system that became Hurricane Helene in 2024. Each ensemble member passes independently through the catastrophe-modeling chain, producing a distribution of possible county losses.

## Project workflow

1. Load and inspect the 50-member hurricane forecast ensemble.
2. Transform forecast data into county-level wind hazard.
3. Combine hazard with residential property exposure.
4. Apply vulnerability relationships to estimate wind damage.
5. Aggregate losses geographically.
6. Calculate and visualize percentile-based Value-at-Risk.

## Skills demonstrated

- Probabilistic weather and ensemble analysis
- Climate-risk and catastrophe modeling
- Geospatial joins and county-level aggregation
- Exposure, vulnerability, and loss modeling
- Tail-risk communication for financial decisions

## Responsible interpretation

This educational model simplifies real catastrophe-risk systems. Its estimates are scenario-dependent and should not be used for underwriting, investment, emergency management, or public-safety decisions without professional validation and higher-quality exposure and vulnerability data.

## Portfolio note and provenance

This repository is my portfolio fork and study implementation of a **Climate Change AI** tutorial. The original notebook, methodology, and scientific content are credited to the creator below.

### Original creator

- Tristan Ballard, PhD — Zeus AI

## Citation

Ballard, T. (2026). *Estimating Hurricane Wind Value-at-Risk from an AI Weather Ensemble* [Tutorial]. Climate Change AI Summer School. https://doi.org/10.5281/zenodo.21828317

```bibtex
@misc{ballard2026hurricane,
  title={Estimating Hurricane Wind Value-at-Risk from an AI Weather Ensemble},
  author={Ballard, Tristan},
  year={2026},
  organization={Climate Change AI},
  type={Tutorial},
  doi={10.5281/zenodo.21828317},
  booktitle={Climate Change AI Summer School},
  howpublished={\url{https://github.com/climatechange-ai-tutorials/hurricane-wind-var}}
}
```

## License

Released under the [MIT License](LICENSE).