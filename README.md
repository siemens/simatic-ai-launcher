
<!--- Copyright 2021 Siemens AG -->
<!--- SPDX-License-Identifier: MIT -->
# Toolbox for SIMATIC AI Launcher

## Content  

This project focuses on the code examples referenced in SIMATIC AI Launcher. An automotive engineer can create and train effective neural networks to use them in the SIMATIC AI setup by following the instructions on the Getting Started pages of the SIMATIC AI Launcher. For a detailed explanation of the example notebooks, and further information, visit our [portal](https://support.industry.siemens.com/cs/ww/en/view/109780569). This project also contains configuration files to build isolated python environments, containing all the necessary packages to execute the IPython notebooks.

## Folder structure:  
- **ai-examples**:  
Main folder for exploratory python scripts on SIMATIC AI Launcher
  - ***.ipynb files**: IPython notebook files containing AI application examples. They are designed to run in JupyterLab.
  - ***.py files**: python files containing utility functions and methods, classes, programs. They are designed to run from command line or IPython notebooks.
- **datasets**:  
This folder contains datasets to support your work with example projects described on the SIMATIC AI Launcher Getting Started Portal. For detailed information, refer to their [Readme](datasets/Readme.md) document.
- **environments**:  
This folder contains the files necessary to build a python environment for running IPython notebooks prepared in the **ai-examples** folder.
  - **conda**: contains an *image-classification.yml* file required to build a Conda virtual environment with the necessary python packages and a *Readme.md* file for guidance
  - **dockerized**: contains an *image-classification.yml* compose file for setting up your container and a *Readme.md* file for guidance
  - **virtualenv**: contains a *Readme.md* to help you setting up your virtual environment
  
# Environment Setup

To avoid changing your working python environment, we provide instructions to build isolated IPython kernels that can run our notebooks through JupyterLab. The kernels can be built using Conda, Docker, or python virtualenv. You can choose the most suitable environment based on your system environment or your preference. Refer to the *Readme.md* file in the respective environment folder for more details about setting up a specific environment.

- The **dockerized** solution contains a basic python environment, including all of the notebook dependencies and a JupyterLab, available on port 8888. This solution requires some engineering knowledge about docker containers, but it is the cleanest option if you do not have JupyterLab already installed on your system.

- The **conda** solution creates a new Conda environment for the given IPython notebook with all the notebook dependencies but without any JupyterLab installation. Choose this option if you already have a python environment with Conda and JupyterLab installed.

- The **virtualenv** solution contains the know-how for creating and using a python virtual environment. In this case you also need to install the notebook-related dependencies manually from a *requirements.txt* file. This is the lightest and most transparent among our solutions.

# Legal information
For licensing information refer to the [LICENSE](LICENSE.md) and [THIRD-PARTY-LICENSES](THIRD-PARTY-LICENSES.md) documents.
