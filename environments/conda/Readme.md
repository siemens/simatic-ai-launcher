<!--- Copyright 2020 Siemens AG -->
<!--- SPDX-License-Identifier: MIT -->

# Using conda

By running the next commands you can create a conda virtual environment with the necessary packages to run the related ipython notebook, and then install this environment as an ipython kernel for your user. We assume you already have conda, and JupyterLab installed on your system. If you haven't got one of these, please refer to the official [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html) and [Conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/) installation guides.

Create and activate the new conda environment:
```commandline
conda env create --file <path-to-ai-toolbox>/environments/conda/image-classification.yml

conda activate image-classification
``` 


Install a new ipython kernel using the freshly created conda environment: (please make sure the kernel name doesn't already exist in your kernel list)
```commandline
python -m ipykernel install --user --name image-classification --display-name "Python (image-classification)"
``` 

Deactivate the conda environment:
```commandline
conda deactivate
```  

The new kernel is now ready to be used from JupyterLab. To run the notebooks, just start up your already installed JupyterLab instance:
```commandline
jupyter lab
``` 