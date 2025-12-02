# Assignment 01

**Author:** Grace Akatsu  
**Course:** CPBS 7602 - Big Data in Biomedical Informatics, Fall 2025  

## Overview

This project performs unsupervised clustering analysis on GTEx (Genotype-Tissue Expression) bulk RNA sequencing data to identify tissue-specific gene expression patterns. The analysis compares K-means and DBSCAN clustering algorithms and evaluates their performance in identifying tissue of origin.

## Project Structure

```
assignment01/
├── README.md                                    # This file
├── environment.yml                              # Conda environment specification
├── 01_data_download_and_preprocessing.ipynb     # Data acquisition and preprocessing
├── 02_cluster_analysis_k_means.ipynb           # K-means clustering analysis
├── 03_cluster_analysis_DBSCAN.ipynb            # DBSCAN clustering analysis  
├── 04_cluster_evaluation_and_interpretation.ipynb # Clustering evaluation and gene analysis
.
.
.
And what will be created:
.
.
.
├── data/                                        # Raw downloaded data
│   ├── GTEx_Analysis_2017-06-05_v8_RNASeQCv1.1.9_gene_tpm.gct.gz
│   └── GTEx_Analysis_v8_Annotations_SampleAttributesDS.txt
├── clean_data/                                  # Processed data
│   └── gtex_top10_tissues_top5000_variable_genes_standardized.csv
├── k_means_outputs/                             # K-means results
│   ├── kmeans_k10_cluster_assignments.csv
│   └── kmeans_k10_cluster_assignments_PCA.png
└── DBSCAN_outputs/                             # DBSCAN results
    ├── dbscan_cluster_assignments.csv
    └── DBSCAN_k10_cluster_assignments_PCA.png



HTML exports of all notebooks are also included in this repo, but will not be automatically generated.
```

## Notebooks Description

- 1. Data Download and Preprocessing (`01_data_download_and_preprocessing.ipynb`)
- 2. K-means Clustering Analysis (`02_cluster_analysis_k_means.ipynb`)
- 3. DBSCAN Clustering Analysis (`03_cluster_analysis_DBSCAN.ipynb`)
- 4. Cluster Evaluation and Interpretation (`04_cluster_evaluation_and_interpretation.ipynb`)

## Reproduction Instructions

### Prerequisites

1. **Python Environment:** Create conda environment from `environment.yml`
   ```bash
   # After cloning and moving into the assignment01 directory:
   
   conda env create -f environment.yml
   conda activate assignment01_env
   ```

2. **Jupyter Setup:** Ensure Jupyter is installed and can access the conda environment
   ```bash
   python -m ipykernel install --user --name assignment01_env --display-name "CPBS 7602 assignment 01: clustering"
   ```

### Step-by-Step Execution

**Important:** Run notebooks in numerical order as each depends on outputs from previous notebooks.

1. **Data Download and Preprocessing**
   ```bash
   jupyter notebook 01_data_download_and_preprocessing.ipynb
   ```

2. **K-means Analysis**
   ```bash
   jupyter notebook 02_cluster_analysis_k_means.ipynb
   ```

3. **DBSCAN Analysis**
   ```bash
   jupyter notebook 03_cluster_analysis_DBSCAN.ipynb
   ```

4. **Evaluation and Interpretation**
   ```bash
   jupyter notebook 04_cluster_evaluation_and_interpretation.ipynb
   ```

### Notes

- **Reproducibility:** Random seed set to 0 on all notebooks for consistent results across runs
- **Data Source:** GTEx v8 public data (https://gtexportal.org/)
