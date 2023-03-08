#
# Setup conda env
#
conda create --name jupyter

conda activate jupyter

#
# Install Jupyter 
#
pip install jupyterlab


#
# Start the jupyter notebook server
#
jupyter-lab

