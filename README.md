# term-project-snowy-plovers
term-project-snowy-plovers created by GitHub Classroom

This repository contains our final project for CS133.  
We analyze Snowy Plover data from Point Reyes National Seashore, including observations, predators, nest outcomes, and banding data. Our project includes data exploration, visualizations, an interactive geomap dashboard, and machine learning models.

---

## Repository Structure

### `code/`
Contains all Python notebooks related to:
- data cleaning and preprocessing  
- exploratory data analysis (EDA)  
- machine learning models
See `data/README.md` for details.
Each notebook can be run independently when the required datasets are available.

### `dashboard/`
Contains the **interactive geomap** created with Folium:
- `plover_map.html` — standalone interactive map (open in any browser)  
- `Interactive_Geomap.ipynb` — notebook that generates the map  
- README with environment setup instructions for running the dashboard

### `data/`
Contains the datasets used in the project:
- `merged_OP.csv` — intermediate dataset used for initial EDA  
- `cleaned_plover_dataset.csv` — final dataset used for ML and the interactive map  
See `data/README.md` for details.

### `homework/`
Archived notebooks from earlier assignments.  
These are **not** used in the final pipeline but are included for reference.

---

## How to Run the Project

To run the notebooks (EDA or ML), you must set up a Python environment and install required libraries.

### Environment Setup

You can use either conda or venv.

#### Using conda:
conda create -n plover-env python=3.10 -y

conda activate plover-env

pip install pandas numpy seaborn matplotlib scikit-learn folium plotly jupyter


#### Using venv (standard Python)

Create the environment:

python -m venv plover-env


Activate the environment:

macOS / Linux:
source plover-env/bin/activate


Windows (PowerShell):
plover-env\Scripts\Activate.ps1

Install the required packages:

pip install pandas numpy seaborn matplotlib scikit-learn folium plotly jupyter
