# Effect of Ageing on Macrophage Transcriptomic Profile
Cross-species computational analysis of ageing in lung macrophages using mouse (Tabula Muris Senis) and human (HCLA) single-cell datasets.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Key Objectives](#key-objectives)
- [Dataset Layers](#dataset-layers)
  - [Layer 1: Mouse (Tabula Muris Senis)](#layer-1-mouse-tabula-muris-senis)
  - [Layer 2: Human Lung (HCLA)](#layer-2-human-lung-hcla)
- [Methods Summary](#methods-summary)
- [Repository Structure](#repository-structure)
- [Installation & Environment](#installation--environment)
- [How to Run the Pipelines](#how-to-run-the-pipelines)
- [Results & Outputs](#results--outputs)
- [Citations](#citations)
- [License](#license)

---

## Project Overview
Ageing alters immune function and cellular identity. This project analyzes how ageing affects **lung macrophage transcriptomes** across species, focusing on alveolar macrophages, interstitial macrophages, and monocyte subsets.

This repository includes:
- Full single-cell RNA-seq preprocessing pipelines  
- Age-stratified differential expression  
- Machine learning models (PLS-VIP, Random Forest, Logistic Regression)  
- Deep generative modelling (scVI/SCANVI)  
- Pathway and GO analysis  
- Cross-species conserved ageing marker discovery  

---

## Key Objectives
- Identify age-associated transcriptional changes in mouse and human macrophages.
- Build machine learning models to predict age from gene expression.
- Compare ageing trajectories across species.
- Generate high-quality figures and reproducible analyses.

---

## Dataset Layers

### Layer 1: Mouse (Tabula Muris Senis)
This layer uses the Tabula Muris Senis FACS + droplet datasets for murine lung macrophage ageing analysis.

Includes:
- Scanpy QC, filtering, normalization  
- PCA, UMAP, Leiden clustering  
- Macrophage subtype annotation  
- Age-stratified differential expression  
- PLS-VIP age-predictive genes  
- Random Forest + Logistic Regression models  
- scVI/SCANVI latent embeddings  
- Pathway enrichment and visualization  

### Layer 2: Human Lung (HCLA)
This layer analyzes human lung macrophages using Human Cell Landscape (HCLA) datasets.

Includes:
- Scanpy pipeline for human lung  
- Macrophage subtype identification  
- Human ageing DEGs  
- ML models applied to human data  
- Human–mouse ortholog mapping  
- Cross-species signature comparison  

---

## Methods Summary

| Category | Methods |
|---------|---------|
| Preprocessing | QC, filtering, normalization (Scanpy) |
| Dimensionality Reduction | PCA, UMAP |
| Clustering | Leiden |
| Machine Learning | PLS-VIP, Random Forest, Logistic Regression |
| Latent Modelling | scVI, SCANVI |
| Differential Expression | Wilcoxon rank-sum |
| Functional Analysis | GO, KEGG, pathway enrichment |
| Visualization | UMAPs, heatmaps, volcano plots, matrixplots |

---

## Repository Structure

