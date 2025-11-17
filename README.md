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
- Single-cell RNA-seq preprocessing  
- Age-stratified differential expression  
- Machine learning models (PLS-VIP, Random Forest, Logistic Regression)  
- Deep generative modelling (scVI/SCANVI)  
- GO and pathway enrichment  
- Cross-species ageing marker analysis  

---

## Key Objectives
- Identify transcriptional changes associated with ageing in macrophages.  
- Build ML models to classify age from transcriptomic profiles.  
- Compare ageing signatures between mouse and human.  
- Detect conserved macrophage ageing markers.  
- Produce reproducible plots, signatures, and reports.  

---

## Dataset Layers

### Layer 1: Mouse (Tabula Muris Senis)
Includes:
- Scanpy-based QC + preprocessing  
- Normalization, HVG selection  
- PCA, UMAP, Leiden clustering  
- Subtype annotation (AM, IM, monocytes)  
- DEGs across age groups  
- PLS-VIP regression  
- Random Forest + Logistic Regression  
- scVI / SCANVI latent ageing models  
- Pathway enrichment  
- Figures (UMAP, heatmap, volcano, matrixplot)  

### Layer 2: Human Lung (HCLA)
Includes:
- Human lung single-cell preprocessing  
- Human macrophage subtype identification  
- Age-stratified DEGs  
- ML models trained on human data  
- Mouse-to-human ortholog mapping  
- Cross-species conserved ageing signatures  
- Functional pathway analysis  

---

## Methods Summary

| Category | Methods |
|---------|---------|
| Preprocessing | Scanpy QC, normalization, filtering |
| Dimensionality Reduction | PCA, UMAP |
| Clustering | Leiden |
| Machine Learning | PLS-VIP, Random Forest, Logistic Regression |
| Deep Models | scVI, SCANVI |
| Differential Expression | Wilcoxon rank-sum |
| Functional Analysis | GO, KEGG, enrichment analyses |
| Visualization | UMAP, volcano, heatmap, matrixplot |

---

## Repository Structure

The following reflects the recommended structure of this project:



