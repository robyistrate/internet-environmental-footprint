# Environmental footprint of Internet consumption

## Description

Repository to share the code used in the scientific article **Istrate *et al.*, On the environmental sustainability of digital content consumption**. The repository contains data files and tailored notebooks to create the LCI database and reproduce the results presented in the article.

The data folder includes:
- `LCI_Digital-Content-Consumption.xlsx` inventory data in a suitable format to be imported into [Brightway2](https://github.com/brightway-lca)
- `LCIA_Carrying-Capacities.xlsx` per capita Earth's carrying capacity for 16 impact categories (only for results analysis)
- `Sensitivity-Analysis-Carbon-Budgets.xlsx` different carbon budgets used for sensitivity analysis (only for results analysis)
- `Sensitivity-Analysis-LCI-for-Presamples.xlsx` inventory data sensitivity analysis in a suitable format to be used with [presamples](https://github.com/PascalLesage/presamples) (only for results analysis)
- `Soil-Erosion-Potential_CFs_LANCA_v2.5.xlsx` characterization factors from the updated LANCA model for land use impact assessment (there is a notebook to update this as well as other methods)

The notebooks folder includes:
- `00_Project_setup.ipynb` creates a new BW2 project, imports the biosphere and ecoinvent databases, creates the prospective databases using [premise](https://github.com/polca/premise), and creates/updates some LCIA methods that are used for results analysis but which are not available by default (i.e., in the biosphere3 database compatible with ecoinvent 3.8).
- `01_Create_LCI_databases.ipynb` creates default and prospective LCI databases for digital content consumption based on the inventory data file.
- `02_LCA_results_analysis.ipynb` produces the results and figures presented in the scientific article.
- `_Functions_to_create_database.ipynb` and `_Functions_for_results_analysis.ipynb` contain all the necessary functions to run the previous notebooks (you do not need to run these notebooks)

## Usage

To ensure the replication of the results presented in the article, it is highly recommended starting a new environment and installing the `requirements.txt`. To do this, run the following lines of code:

```
conda create -n ef_internet python==3.10.2
conda activate ef_internet
cd your/repository
pip install -r requirements.txt
```

Once in the new environment, run the notebooks following the order described above. Further details are provided in the corresponding notebooks

## DOI

Version identifier: ![DOI](https://zenodo.org/badge/7575568.svg)



