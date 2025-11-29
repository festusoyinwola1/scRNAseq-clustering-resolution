# scRNAseq-clustering-resolution
Analysis of how Leiden clustering resolution affects inferred cell types in a single-cell RNA-seq dataset.

# scRNAseq-clustering-resolution

# Overview
This project evaluates how varying Leiden clustering resolution (0.2, 0.5, 2.0) influences the identification of cell types in a single-cell RNA sequencing (scRNA-seq) dataset. The goal is to understand how clustering parameters affect cluster granularity, marker-gene stability, and downstream biological interpretation.

# Biological Question
How does Leiden clustering resolution affect the number of inferred cell types and the stability of marker genes in a standard scRNA-seq dataset?

# Data
- **Source:** Public Scanpy tutorial dataset (AnnData example)
- **Format:** Processed .h5ad count matrix
- **Size:** ~3,000–5,000 cells with several thousand genes
- **Preprocessing:** QC, normalization, log-transform, PCA, and kNN graph included in the dataset

# Methods
- Load .h5ad dataset using Scanpy
- Confirm preprocessing steps (PCA, neighbors)
- Perform Leiden clustering at **0.2**, **0.5**, and **2.0**
- Generate UMAP visualizations for each resolution
- Extract marker genes per cluster
- Evaluate cluster separability with Scanpy’s classifier
- Prepare results tables and figures for the final report

# Repository Structure
scRNAseq-clustering-resolution/
- # data/
- cluster_counts_by_resolution.csv
- cluster_separability_scores.csv
- marker_genes_leiden_0.5.csv
- # figures/
- umap_leiden_0.2.png
- umap_leiden_0.5.png
- umap_leiden_2.0.png
- # notebooks/
- Finalproject.ipynb
- # README.md
- # ai_usage.md
- # scripts/
- placeholder.txt

## Timeline (Draft)
- **Week 1:** Baseline workflow tested; data loaded; PCA and neighbors validated (completed)
- **Week 2:** Run Leiden clustering for 0.2, 0.5, and 2.0; generate corresponding UMAPs (In progress)
- **Week 3:** Identify marker genes; evaluate classifier; build figures; finalize report and GitHub repo

## Reproducibility
- All analysis steps will be documented in Jupyter notebooks under /notebooks
- Instructions and project description provided in this README.md
- Repository includes all required components for transparency and reproducibility

## AI Use
See ***ai_usage.md*** for documentation of ChatGPT/Gemini usage, verification steps, and transparency notes.


# Note: GitHub may not render the notebook preview correctly. To view and run the analysis, download notebooks/FinalProject.ipynb and open it in Google Colab.
