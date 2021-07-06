
# State Identifier dataset

This folder contains multi-variate time series measurements, which function as example datasets for the templates provided by AI Designer.

## File format and naming

The folder contains two `parquet` files which is a binary format for storing columnar data.
This format is designed to speed up column-related data processes, but also usable by pandas DataFrame.  

The `si-sample.parquet` is the original dataset with three measured variables with a timestamp value. This file is used by the unsupervised training notebooks in the State Identifier template of AI Designer.  

The `si-sample-with-labels.parquet` file contains the same data, but it is extended with a `class` column which is the state we want to recognize. This file is used by the supervised training notebooks in the State Identifier template of AI Designer.

## Data columns

The three measured values represent the energy consumption in a machine on the shopfloor. These values will be used in the template notebooks of AI Designer. These introduce you to the workflow from collecting data to creating a configuration package with a created model.

In both files:
  - **DateTime**  (String): the timestamp when the values are measured 
  - **ph1** (Double): measured value on energy consumption in phase 1
  - **ph2** (Double): measured value on energy consumption in phase 2
  - **ph3** (Double): measured value on energy consumption in phase 3  

Only in si-sample-with-labels.parquet`:  
  - **class** (Integer): known state of the machine at the given timestamp   
 