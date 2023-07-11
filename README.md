[![DOI](https://zenodo.org/badge/594736106.svg)](https://zenodo.org/badge/latestdoi/594736106)

# Equity Measurements 
## Overview
This repository includes all data and code to reproduce the data analysis and figures from Pollack et al (2023), "Designing equity indicators to support flood-risk management."
## Data
The /data folder includes five .csv files.

1) all_papers.csv includes every study returned from the search query to web of science, and all of the fields recorded for each study. 
2) all_papers_col_map.csv maps each column name from all_papers.csv to a detailed explanation of the field
3) measure_equity.csv includes every measurement of the distribution of an outcome (subset matches equity_measured field of all_papers.csv) and all of the fields recorded, including whether the measurement is an equity indicator or not. 
4) measure_equity_col_map.csv maps each column name from measure_equity.csv to a detailed explanation of the field
5) unique_techniques.csv tracks methods used to measure the distribution of an outcome for all the studies in measure_equity.csv

## Code
The /env folder includes the .yml file that can set up the conda environment required to run the Jupyter Notebook and execute all of the code.

The /src folder includes the Jupyter Notebook.

## Reproduce Me
Check that conda is installed on your system
1. Clone the repository into a local project directory
2. In your local project directory, run `conda env create -f environment.yml`
3. When the environment is created, you can launch a Jupyter Notebook and open src/EquityReview.ipynb
    * This step assumes some experience with using ipykernel to use a specific conda environment in a Jupyter Notebook. If you are new to Jupyter Notebooks and/or conda, please see: https://ipython.readthedocs.io/en/stable/install/kernel_install.html#kernels-for-different-environments 


You can run all cells in the Jupyter Notebook. Figures are generated twice - once with readable font size, and once with very small labels. The purpose of this is to manually arrange the figures with legible labels, and then repeat the visual apperance of that plot with the "invisible" labels. The latters plot were downloaded as a .png and edited in Keynote to re-add labels. The built-in function for producing the parallel categories plots is hard to optimize for labels and arrangement of bars and this process was easier to customize. 

Please contact Adam Pollack at adam.b.pollack@dartmouth.edu if you have any issues following these steps. 
