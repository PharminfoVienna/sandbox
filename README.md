# Sandbox
The PharminfoVienna Sandbox is a tool combining data gathering using KNIME and model building of classification models using Jupyter Notebook.

# Data Gathering KNIME Workflow
The KNIME workflow (WF) handles all steps of dataset generation automatically, the
workflow only needs minimal input which can be configured by using a graphical user interface.
The gathered datasets can be downloaded and used for further modeling with the PharminfoVienna Sandbox.

# Setting up KNIME
Knime is a free open-source data science software which allows the easy creation of workflows without the need of any programming skills. 
## Step 0: Preparation
- Set up a local ChEMBL instance
- Set up a Python Environment

A detailed description can be found [here](https://hub.docker.com/r/pharminfovienna/sandbox).
## Step 1: Download KNIME
You can download KNIME [here](https://www.knime.com/downloads/download-knime).
Choose the correct version for your operating system and follow the installation instructions.
## Step 2: Import the Workflow
Go to *File* -> *Import KNIME Workflow*
At the appearing *Import* window, choose *Select file* and browse to the *.knwf-File
## Step 3: Set up Python Environment
The standardization of the compounds requires certain python libraries therefore KNIME needs to access the previously installed Environment (see *Step 0* - *Set up Python Environment*).

```conda create -n sandbox-env python=3.6```

```conda activate sandbox-env```

```conda install -c rdkit rdkit=2020.03.2.0```

<b>Alternative for Linux:</b>

```conda env create -f environment.yml```

```conda activate sandbox-env```


## Step 4: Configuration of the Workflow
A detailed description including illustrations of the different steps are given in the file: <b>*documentation_data_gathering_sandbox.docx*</b> 


# PharminfoVienna Sandbox (Sandbox Docker)
[See at DockerHub](https://hub.docker.com/r/pharminfovienna/sandbox) 
