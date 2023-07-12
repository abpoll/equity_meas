[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.8139215.svg)](https://doi.org/10.5281/zenodo.8139215)

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

The /src folder includes the Jupyter Notebook. All code is written in python. 

## Reproduce Me
Check that conda is installed on your system. I used version 22.11.1 for the build which may be helpful to install for reproduction purposes to make sure you can build the environment successfully. Once you are ready to proceed:  

1. Clone the repository into a local project directory
2. In your local project directory, run 'cd env' and then run `conda env create -f environment.yml`
3. When the environment is created, you can launch a Jupyter Notebook and open src/EquityReview.ipynb. Be sure to 'eqmeas' (or, if you changed the name of the environment when you created the conda environment, be sure to set the kernel to that environment)
    * This step assumes some experience with using ipykernel to use a specific conda environment in a Jupyter Notebook. If you are new to Jupyter Notebooks and/or conda, please see: https://ipython.readthedocs.io/en/stable/install/kernel_install.html#kernels-for-different-environments

You can run all cells in the Jupyter Notebook. Figures are generated twice - once with readable font size, and once with very small labels. The purpose of this is to manually arrange the figures with legible labels, and then repeat the visual apperance of that plot with the "invisible" labels. The latters plot were downloaded as a .png and edited in Keynote to re-add labels. The built-in function for producing the parallel categories plots is hard to optimize for labels and arrangement of bars and this process was easier to customize. 

The Notebook is organized as follows, with brief overviews of what the code in each section does:
1. Import libraries for loading data, obtaining summary statistics, and producing visualizations
2. Load review data
  * This includes some cleaning of csvs (excess rows and columns)
3. Summarize review
  * Filters described in the supplementary information are conducted
4. Summarize review sample definitions
  * Summarize how equity is defined in full sample of studies
5. Summarize qualitative papers definitions
  * For the qual studies, summarize definitions
6. Summarize quantitative papers definitions
  * For the quantitative studies, summarize definitions
  * See how many quant. studies that have definitions define indicators
7. Map indicators onto taxonomy
  * Summary statistics on indicators reported in the text are produced here
  * A second figure is produced with small text for editing outside the constraints of plotly customizability options
8. Compare equity indicators with similar measurements
  * Map stated equity measurements to the taxonomy as well
  * Also includes the generation of a second figure

Note that not all cells will result in output. The key results are in sections 7 & 8, and there are some values printed to the console in sections 3-6. 

So far, these instructions have resulted in successful reproduction of the figures and summary statistics reported in the manuscript, but you may run into issues and need assistance debugging. Please contact Adam Pollack at adam.b.pollack@dartmouth.edu if you have any issues following these steps. 
