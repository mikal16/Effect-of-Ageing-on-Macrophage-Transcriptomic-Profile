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

Effect-of-Ageing-on-Macrophage-Transcriptomic-Profile/
│
├── mouse_tabula_muris/
│ ├── Lung_Macrophages_Scanpy_General_Pipeline.ipynb
│ ├── PLS-Tabula-Muris-Pipeline.ipynb
│ ├── PLS-Tabula-Muris-RandomForest.ipynb
│ ├── Tabula-Muris-PLS-RF-LogRegr-Model.ipynb
│ ├── unagi-pipeline-working-copy.ipynb
│ └── sccellfie-metabolite-analysis.ipynb
│
├── human_hcla/
│ ├── HCLA-Lung-Scanpy-Pipeline.ipynb
│ ├── HCLA-PLS-RF-LogisticRegression.ipynb
│ └── Cross-Species-Analysis.ipynb
│
├── results/
│ ├── PLS_VIP_gene_lists/
│ ├── RandomForest_feature_importance/
│ ├── DEG_results/
│ └── figures/
│
└── README.md



---

## Installation & Environment

### Conda Installation
```bash
conda create -n macrophage-ageing python=3.10
conda activate macrophage-ageing
pip install scanpy scvi-tools scikit-learn pandas numpy seaborn matplotlib anndata gseapy
pip install torch torchvision torchaudio


## How to Run the Pipelines

### 1. Clone the repository
    git clone https://github.com/<your-username>/Effect-of-Ageing-on-Macrophage-Transcriptomic-Profile
    cd Effect-of-Ageing-on-Macrophage-Transcriptomic-Profile

### 2. Add datasets
Place all mouse and human data under:

    data/
        tabula-muris-senis/
        hcla-lung/

### 3. Launch Jupyter
    jupyter lab

### 4. Run notebooks
Execute the notebooks located in:

- mouse_tabula_muris/
- human_hcla/

---

## Results & Outputs

### Mouse Layer
- Age-stratified DEGs
- PLS-VIP age-predictive signatures
- Random Forest feature importance
- scVI latent embeddings
- UMAP visualizations
- Volcano plots and heatmaps
- GO/KEGG enrichment outputs

### Human Layer
- Human macrophage ageing markers
- Machine learning performance metrics
- Mouse–human ortholog mapping
- Conserved ageing signatures
- Pathway-level ageing shifts

---

## Citations

**Tabula Muris Senis**  
Tabula Muris Consortium, *Nature*, 2020.

**Human Cell Landscape (HCL/HCLA)**  
HCL Consortium, *Nature*, 2021.

