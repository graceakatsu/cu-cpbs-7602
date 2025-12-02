# Assignment 02

**Author:** Grace Akatsu  
**Course:** CPBS 7602 - Big Data in Biomedical Informatics, Fall 2025  

## Overview

This project****

## Project Structure

```
assignment02/
├── README.md                                    # This file
├── environment.yml                              # Conda environment specification
.
.
.
And what will be created:
.
.
.
├── data/                                        # Raw downloaded data
│   ├── GTEx_Analysis_2017-06-05_v8_RNASeQCv1.1.9_gene_tpm.gct.gz
│   ├── GTEx_Analysis_v8_Annotations_SampleAttributesDS.txt
│   └── GTEx_Analysis_v8_Annotations_SubjectPhenotypesDS.txt
├── clean_data/                                  # Processed data
│   └── gtex_blood_brain_top5000_variable_genes_standardized.csv
├── ****                            
│   ├── ****
│   └── ****
└── ****                        
    ├── ****
    └── ****


```

## Notebooks

- 1) Data Download and Preprocessing (`01_data_download_and_preprocessing.ipynb`)

## Reproduction Instructions

### Prerequisites

1. **Python Environment:** Create conda environment from `environment.yml`
   ```bash
   # After cloning and moving into the assignment01 directory:
   
   conda env create -f environment.yml
   conda activate assignment02_env
   ```

2. **Jupyter Setup:** Ensure Jupyter is installed and can access the conda environment
   ```bash
   python -m ipykernel install --user --name assignment02_env --display-name "CPBS 7602 assignment 01: clustering"
   ```

### Step-by-Step Execution

**Important:** Run notebooks in numerical order as each depends on outputs from previous notebooks.

1. **Data Download and Preprocessing**
   ```bash
   jupyter notebook 01_data_download_and_preprocessing.ipynb
   ```

2. 

### Notes

- **Reproducibility:** Random seed set to 0 on all notebooks for consistent results across runs
- **Data Source:** GTEx v8 public data (https://gtexportal.org/)
