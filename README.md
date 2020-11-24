<!--- Copyright 2020 Siemens AG -->
<!--- SPDX-License-Identifier: MIT -->
# Toolbox for SIMATIC AI Launcher

## Content  

This project focuses on the code examples referenced in SIMATIC AI Launcher. An automotive engineer can create and train effective neural networks that can be used in the SIMATIC AI setup by following the instructions on the Getting Started pages of the SIMATIC AI Launcher. For a detailed explanation of the example notebooks, and further information please visit our [portal](https://support.industry.siemens.com/cs/ww/en/view/109780569). This project also contains configuration files to build isolated python environments, containing all the necessary packages to execute the ipython notebooks.

## Folder structure:  
- **ai-examples**:  
Main folder for exploratory python scripts on SIMATIC AI Launcher
  - ***.ipynb files**: IPython notebook files containing AI application examples. They are designed to run in JupyterLab.
  - ***.py files**: python files containing utility functions and methods, classes, programs. They are designed to run from command line or ipython notebooks.
- **datasets**:  
This folder contains datasets to train networks created in **ai-examples** folder.
- **environments**:  
This folder contains necessary files to build python environment to run ipython notebooks prepared in the **ai-examples** folder.
  - **dockerized**: contains file(s) necessary to run docker image which is able to run JupyterLab and notebooks
  - **virtualenv**: contains *requirements.txt* file required to build python environment with certain versions of python packages used in ipython notebooks
  - **conda**: contains *environment.yaml* file required to build conda virtual environment with necessary python packages

# Environment Setup

To avoid changing your working python environment, we provide instructions to build isolated ipython kernels that can run our notebooks through JupyterLab. The kernels can be built using Conda, Docker, or python virtualenv. You can choose the most suitable environment based on your system environment or your taste. Please see the readme files in the environment folder for more details about setting up a specific environment.

- The **dockerized** solution contains a basic python environment, including all of the notebook dependencies and also JupyterLab, available on port 8888. This solution requires some engineering knowledge about docker containers but it is the cleanest option if you haven't already got JupyterLab installed.

- The **conda** solution creates a new conda environment for the given ipython notebook with all the notebook dependencies but without any JupyterLab installation. You should choose this option if you already have a python environment with conda and JupyterLab installed.

- The **virtualenv** solution contains the know how about creating and using a python virtual environment. In this case you also need to install the notebook related dependencies manually from a requirements.txt file. This is the lightest and most transparent among our solutions.

# Legal information
For licensing information please refer to the [LICENSE](LICENSE.md) and [THIRD-PARTY-LICENSES](THIRD-PARTY-NOTICES.md) documents.
