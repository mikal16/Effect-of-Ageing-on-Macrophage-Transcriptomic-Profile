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

---

## Project Overview
Ageing alters immune function and cellular identity. This project analyzes how ageing affects **lung macrophage transcriptomes** across species, focusing on alveolar macrophages, interstitial macrophages, and monocyte subsets.

This repository includes:
- Single-cell RNA-seq preprocessing  
- Age-stratified differential expression  
- Machine learning models (PLS-VIP, Random Forest, Logistic Regression)  
- Deep generative modelling (scVI/SCANVI)  
- GO and pathway enrichment  
- Cross-species ageing marker analysis  

The goal is to define how ageing remodels macrophage biology in both **mouse** and **human**, and identify conserved age-associated signatures.

---

## Key Objectives
- Identify transcriptional changes associated with ageing in macrophages.  
- Build ML models to classify age from transcriptomes.  
- Compare ageing signatures between mouse and human.  
- Detect conserved macrophage ageing markers.  
- Produce publication-quality plots and reproducible analyses.  

---

## Dataset Layers

### Layer 1: Mouse (Tabula Muris Senis)
Includes:
- Scanpy QC, filtering, normalization  
- HVG selection, PCA, UMAP, Leiden clustering  
- Macrophage subtype annotation (AM, IM, monocytes)  
- Age-stratified DEGs  
- PLS-VIP age-predictive genes  
- Random Forest & Logistic Regression models  
- scVI/SCANVI latent modelling  
- GO/KEGG enrichment  
- Comprehensive visualizations (volcano, heatmaps, UMAPs)  

### Layer 2: Human Lung (HCLA)
Includes:
- Scanpy preprocessing  
- Human macrophage subtype identification  
- Age-based DEGs  
- ML models on human data  
- Mouse–human ortholog mapping  
- Cross-species conserved ageing markers  
- Pathway enrichment analyses  

---

## Methods Summary

| Category | Methods |
|---------|---------|
| Preprocessing | Scanpy QC, filtering, normalization |
| Dimensionality Reduction | PCA, UMAP |
| Clustering | Leiden |
| Machine Learning | PLS-VIP, Random Forest, Logistic Regression |
| Deep Models | scVI, SCANVI |
| Differential Expression | Wilcoxon rank-sum |
| Functional Analysis | GO, KEGG |
| Visualization | UMAPs, heatmaps, volcano plots, matrixplots |

---
