#
# Setup conda env and use Python version 3.9
#
conda create --name jupyter python=3.9

conda activate jupyter

#
#
#
conda install -c conda-forge ipywidgets

#
# Install Jupyter 
# See also https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html
# 
conda install -c conda-forge jupyterlab

#
# Start the jupyter notebook server
#
jupyter-lab


#
# On Mac M1 processors you need to have the arm64 lib versions
# This is how you can install them.
#
pip uninstall hnswlib
ARCHFLAGS="-arch arm64" pip install hnswlib --compile --no-cache-dir