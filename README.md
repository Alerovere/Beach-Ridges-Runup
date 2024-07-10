README
To run the notebooks, the best way is to install three separate environments in Anaconda, to avoid conflicts between versions of libraries required.

# Install the Copernicus Marine Service Toolbox
Make a new environment (python 3.11.X) and use this command in the conda terminal:
conda install conda-forge::copernicusmariyne --yes
conda install ipykernel
conda install notebook -y

In the same environment, install the pyTMD tidal prediction software
conda install -c conda-forge pytmd

Also install:
windrose: pip install windrose
cartopy: pip install Cartopy
astropy: pip install astropy --upgrade

For the tidal predictions to work, you will need to download the FES2014 tidal model. The FES2014 model can be downloaded (upon registration) from the Aviso+ website (https://www.aviso.altimetry.fr/en/data/products/auxiliary-products/global-tide-fes/description-fes2014.html) and should be placed in the "aviso-fes-main" folder.  

# Install the CoastSat Toolbox
Run these commands one by one to create a coastsat environment and install CoastSat

conda create -n coastsat
conda activate coastsat
conda install -c conda-forge geopandas -y
conda install -c conda-forge earthengine-api scikit-image matplotlib astropy notebook -y
pip install pyqt5 imageio-ffmpeg

Download CoastSat from here: https://github.com/kvos/CoastSat.git and unzip its contents into the CoastSat-master folder.

Inside the CoastSat-master folder, you will need to place CoasSat.slope in the "CoastSat.slope-master" folder. CoasSat.slope can be downloaded from here: https://github.com/kvos/CoastSat.slope.git

# Install py-wave-runup
Make a new conda environment, with python 3.11.x. 

Then run these commands in the anaconda prompt: 
conda install pandas numpy notebook -y
pip install -U scikit-learn
pip install seaborn




