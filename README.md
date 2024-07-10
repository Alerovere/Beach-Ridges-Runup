# Beach Ridges Runup

This repository contains a series of Jupyter notebooks designed to calculate the indicative meaning of beach ridges for paleo sea-level studies. To run the notebooks, it is recommended to install three separate environments in Anaconda to avoid conflicts between library versions.

## Installation

### 1. Install the Copernicus Marine Service Toolbox

1. Create a new environment (Python 3.11.x) and use the following commands in the conda terminal:
    ```bash
    conda create -n copernicus python=3.11
    conda activate copernicus
    conda install conda-forge::copernicusmariyne --yes
    conda install ipykernel
    conda install notebook -y
    conda install -c conda-forge pytmd
    pip install windrose
    pip install cartopy
    pip install astropy --upgrade
    ```

2. Download the FES2014 tidal model from the [Aviso+ website](https://www.aviso.altimetry.fr/en/data/products/auxiliary-products/global-tide-fes/description-fes2014.html) (registration required) and place it in the `aviso-fes-main` folder.

### 2. Install the CoastSat Toolbox

1. Create a new environment and install CoastSat:
    ```bash
    conda create -n coastsat python=3.11
    conda activate coastsat
    conda install -c conda-forge geopandas -y
    conda install -c conda-forge earthengine-api scikit-image matplotlib astropy notebook -y
    pip install pyqt5 imageio-ffmpeg
    ```

2. Download CoastSat from [GitHub](https://github.com/kvos/CoastSat.git) and unzip its contents into the `CoastSat-master` folder.

3. Download `CoastSat.slope` from [GitHub](https://github.com/kvos/CoastSat.slope.git) and place it in the `CoastSat.slope-master` folder.

### 3. Install py-wave-runup

1. Create a new environment with Python 3.11.x:
    ```bash
    conda create -n pywaverunup python=3.11
    conda activate pywaverunup
    conda install pandas numpy notebook -y
    pip install -U scikit-learn
    pip install seaborn
    ```

## How to Use

The workflow consists of three steps:

1. Run the `Step 1 - Waves_and_Tides.ipynb` notebook in the main folder of the repository.
2. Run the `Step 2 - Beach slope.ipynb` notebook located in the `CoastSat-master` folder.
3. Run the `Step 3 - Runup.ipynb` notebook located in the `py-wave-runup-master` folder.

Each notebook produces files that are used in the subsequent step.

## Applications

This workflow was tested in a paper in preparation by Rovere et al. If you use this repository for your research, please send your papers to [alessio.rovere@unive.it](mailto:alessio.rovere@unive.it).



