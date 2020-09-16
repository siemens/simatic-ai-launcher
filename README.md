<!--- Copyright 2020 Siemens AG -->
<!--- SPDX-License-Identifier: MIT -->
# Overview

## Content  

This project focuses on the code examples referenced in SIMATIC AI Portfolio. An automotive engineer can create and train effective neural networks which can be used in the SIMATIC AI ecosystem by following the instructions on the Getting Started pages of the AI Portfolio. For further information please read our [SIMATIC AI Portfolio portal](https://support.industry.siemens.com/cs/dl-media/109780569/AI_Portfolio/start.html?lang=en). The project also contains some configuration file for each example to build a tested environment where the ipython notebooks can be executed.  

## Folder structure:  
- **ai-examples**:  
Main folder for exploratory python scripts on SIMATIC AI Portfolio
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

All notebooks can be opened using Google Colab or in a local environment using Conda, Docker, or python virtualenv. Please see the readme files in the environment folder for more details about setting up a local environment

# Usage

All environments described above contain Jupyterlab. all notebooks can be opened and executed using the JupyterLab webUI (port 8888 by default).
