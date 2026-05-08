Baleen Whale SPUE Analysis Repository

OVERVIEW
This repository contains the code and workflow used for Conor Nixon's Master's thesis examining seasonal and interannual patterns of baleen whale occurrence in the Mid-Atlantic Bight using NOAA Northeast Fisheries Science Center aerial survey data from 2023–2024.

The project focuses primarily on fin whales, humpback whales, and North Atlantic right whales. The analysis uses sightings per unit effort (SPUE), spatial heatmaps, seasonal comparisons, depth-binned summaries, and oceanographic context products to investigate whale distributions across the continental shelf and shelf break regions.

REPOSITORY STRUCTURE
- notebooks/
  Main Jupyter notebook containing the full analysis workflow.

- data/
  Directory for input datasets. Large datasets should be linked or documented rather than committed directly.

- figures/
  Exported maps, plots, and thesis figures.

- outputs/
  Processed tables, statistical summaries, and analysis outputs.

- requirements.txt
  Python package requirements.

- NixMoo.yml
  Conda environment specification.

DATA SOURCES
Primary datasets include:
- NOAA NEFSC aerial survey observations
- Survey effort distance calculations
- GEBCO bathymetry products
- DOPPIO oceanographic model outputs
- Survey leg-distance file (Used for effort standardization were generated using processing code developed by Delphine Mossman.)

GEBCO Bathymetry Source:
GEBCO Compilation Group (2024) GEBCO 2024 Grid.
https://www.gebco.net

Large datasets were not included directly in this repository. They should be accessed through their original providers or documented external storage locations. Any derived or smaller processed files needed to rerun the notebook should be placed in the data/ directory.

REPRODUCIBILITY
The notebook is organized so the setup, constants, paths, and data-loading steps occur at the beginning of the workflow. Later sections use those loaded data objects for calculations, figures, and statistical summaries.

To reproduce the analysis:

conda env create -f NixMoo.yml
conda activate whale_spue_analysis
jupyter lab

Then open:
notebooks/baleen_whale_spue_analysis.ipynb

and run the notebook from top to bottom.

MAIN FINDINGS
The analysis identified seasonal and interannual variability in baleen whale occurrence across the Mid-Atlantic Bight. Fin whales and humpback whales showed elevated occurrence in shelf break and outer shelf environments, while right whale occurrence was more spatially restricted and seasonally variable.

Spatial patterns around Hudson Canyon and adjacent shelf break environments suggested that whale occurrence varied alongside environmental structure, including temperature, productivity, and frontal activity.
