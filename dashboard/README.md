# Interactive Geomap Dashboard – README

This folder contains the interactive geomap component of our project. The map was created using Folium and visualizes Snowy Plover activity and nesting metrics across Point Reyes.

## Files

- plover_map.html  
  HTML map that can be opened directly in any web browser.  
  Does not require Python or the dataset to view.

- Interactive_Geomap.ipynb  
  Jupyter Notebook used to generate the geomap. Requires the cleaned dataset ( in the data folder of our project).

## Dataset Requirement (for running the notebook)

To run the notebook and regenerate the map, download the following csv: 

data/cleaned_plover_dataset.csv

The notebook expects a path such as (add to Google Drive):

"/content/drive/MyDrive/Snowy Plover Datasets/cleaned_plover_dataset.csv"


Update the path inside the notebook if your dataset is stored elsewhere.

## Environment Setup

To run the interactive dashboard notebook, you need a Python environment with a few required libraries.
You may use either **conda** or **venv**.

---

### Using conda

If you have Anaconda or Miniconda installed, run the following in your terminal:

conda create -n plover-env python=3.10 -y

conda activate plover-env

pip install folium pandas numpy jupyter

---

### Using venv (standard Python)

If you do not use conda, you can create a virtual environment with `venv`:

Create the environment:

python -m venv plover-env

Activate the environment:

macOS / Linux:  
source plover-env/bin/activate

Windows (PowerShell):  
plover-env\Scripts\Activate.ps1

Install required packages:

pip install folium pandas numpy jupyter

## Running the Notebook

1. Activate your environment  
2. Launch Jupyter Notebook:
   jupyter notebook
3. Open Interactive_Geomap.ipynb  
4. Confirm the dataset path  
5. Run all cells to rebuild the map  
6. The map is saved using:
   plover_map.save("plover_map.html")

## What the Map Shows

- Each bubble represents a beach or survey location  
- Bubble size reflects a plover activity index (total plovers, nest density, and nest success)  
- Clicking a bubble displays detailed metrics  
- The map supports panning, zooming, and interactive inspection of locations
