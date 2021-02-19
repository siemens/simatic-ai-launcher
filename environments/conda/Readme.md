<!--- Copyright 2020 Siemens AG -->
<!--- SPDX-License-Identifier: MIT -->

# Using Conda

By running the next commands you can create a Conda virtual environment with the necessary packages to run the related IPython notebook, and then install this environment as an IPython kernel for your user. We assume you already have Conda, and JupyterLab installed on your system. If either of these is missing, refer to the official [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html) and [Conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/) installation guides.

Create and activate the new Conda environment:
```commandline
conda env create --file <path-to-ai-toolbox>/environments/conda/image-classification.yml

conda activate image-classification
``` 

Install a new IPython kernel using the freshly created Conda environment (make sure the kernel name does not already exist in your kernel list):
```commandline
python -m ipykernel install --user --name image-classification --display-name "Python (image-classification)"
``` 

Deactivate the Conda environment:
```commandline
conda deactivate
```  

The new kernel is now ready to be used from JupyterLab. To run the notebooks, just start up your already installed JupyterLab instance:
```commandline
jupyter lab
``` 