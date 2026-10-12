# Reproducible analysis notebooks

This directory contains three analysis notebooks organized around the three research questions in the manuscript.

1. `01_taxonomic_food_webs.ipynb` — construction and analysis of temporally resolved taxonomic food webs, taxonomic null models, and the supplementary cumulative taxonomic network.
2. `02_functional_projection_and_turnover.ipynb` — functional projection, functional null models, and taxonomic versus trophic-functional temporal turnover.
3. `03_environmental_associations.ipynb` — reduced environmental PCA, environmental-distance/turnover analyses, selected environment–network models, and the AR(1) sensitivity analysis.

## Input files

The notebooks use the audited CSV files referenced by the final analysis. By default, input and generated CSV files are read from and written to the current working directory. Set the environment variable `FOODWEB_DATA_DIR` to point to another directory if needed.

Core audited inputs include:

- `FW_lagoon_nodes_AUDITED.csv`
- `FW_lagoon_trophic_links_AUDITED.csv`
- `FW_lagoon_food_web_by_sampling_AUDITED.csv`
- `FW_lagoon_food_web_metrics_by_sampling_AUDITED.csv`
- `FW_lagoon_functional_links_AUDITED.csv`
- `stage4A_pairwise_dissimilarity.csv`

Notebook 2 consumes intermediate outputs produced within its own workflow and taxonomic outputs produced by Notebook 1. Notebook 3 uses turnover outputs from Notebook 2 and observed network-metric outputs from Notebooks 1–2. Running the notebooks in numerical order is therefore recommended.

## Software

The analysis uses Python with `pandas`, `numpy`, `networkx`, `scipy`, `scikit-learn`, `statsmodels`, `matplotlib`, and `infomap`. Exact package versions can be frozen in a repository environment file before archival.

## Scope

The notebooks contain the analyses retained in the revised manuscript. Exploratory tests, superseded model variants, and development notebooks are not included. Cumulative networks are retained only as supplementary descriptive representations and are not used for temporal inference.
