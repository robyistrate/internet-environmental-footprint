# Environmental footprint of digital content consumption

## Description

Repository to share the code used in the scientific article **Istrate *et al.*, The role of digital content consumption in environmentally sustainable lifestyles**. The repository contains data files and tailored notebooks to create the LCI database and perform the LCIA calculations.

The data container include:
- `LCI_Digital-Content-Consumption.xlsx` inventory data in a suitable format to be imported into [Brightway2](https://github.com/brightway-lca)
- `LCIA_Carrying-Capacities.xlsx` per capita Earth's carrying capacity for the 16 impact categories included in the Environmental Footprint methods (used for results analysis only)

The notebooks container includes:
- `00_Project_setup.ipynb` creates a new BW2 project, imports the biosphere and ecoinvent databases, creates the prospective databases using [premise](https://github.com/polca/premise), and creates/updates some LCIA methods that are used for results analysis but which are not available by default (i.e., in the biosphere3 database compatible with ecoinvent 3.8).
- `01_Create_LCI_databases.ipynb` creates default and prospective LCI databases for digital content consumption based on the inventory data file.
- `02_LCA_results_analysis.ipynb` produces the results and figures presented in the scientific article.
- `_Functions_to_create_database.ipynb` and `_Functions_for_results_analysis.ipynb` contain all the necessary functions to run the previous notebooks (you do not need to run these notebooks)

## Usage

To ensure the replication of the results presented in the paper, it is highly recommended starting a new environment and installing the `requirements.txt`. To do this, run the following lines of code:

```
conda create -n ef_internet
conda activate ef_internet
conda cd your/repository
pip install -r requirements.txt
```

Once in the new environment, just run the notebooks following the order described above

