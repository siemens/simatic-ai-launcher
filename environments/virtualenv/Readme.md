<!--- Copyright 2020 Siemens AG -->
<!--- SPDX-License-Identifier: MIT -->

# Using python virtualenv

By running the next commands you can create a conda virtual environment with the necessary packages to run the related IPython notebook, and then install this environment as an IPython kernel for your user. We assume you already have Python 3.7, virtualenv, and JupyterLab installed on your system. If any of these is missing, refer to the official [Python](https://www.python.org/downloads/), [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html) and [virtualenv](https://virtualenv.pypa.io/en/latest/installation.html) installation guides. Make sure to use Python version 3.7.* or older. The newer Python releases do not support the version of TensorFlow used in our examples.

Create and activate the new virtualenv environment:
```commandline
python -m venv <path_to_new_virtual_environment>

<path_to_new_virtual_environment>/Scripts/activate.bat
```
On a **Linux** distribution instead of */Scripts/activate.bat*, use */bin/activate*.

Install required python packages from *requirements.txt* in *image-classification* directory:
```commandline
pip install -r <path-to-ai-toolbox>/ai-examples/image-classification/requirements.txt
```
Install a new IPython kernel using the freshly created virtualenv environment (make sure the kernel name does not already exist in your kernel list):
```commandline
pip install ipykernel==5.3.0

python -m ipykernel install --user --name image-classification --display-name "Python (image-classification)"
``` 
Deactivate the virtual environment:
```commandline
<path_to_new_virtual_environment>/Scripts/deactivate.bat
```
On a **Linux** distribution instead of */Scripts/deactivate.bat*, use */bin/deactivate*.

The new kernel is now ready to be used from JupyterLab. To run the notebooks, just start up your already installed JupyterLab instance:
```commandline
jupyter lab
``` 
