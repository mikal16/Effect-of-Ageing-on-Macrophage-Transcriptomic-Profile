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

## Repository Structure

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

yaml
Copy code

---

## Installation & Environment

### Using Conda
```bash
conda create -n macrophage-ageing python=3.10
conda activate macrophage-ageing
pip install scanpy scvi-tools scikit-learn pandas numpy seaborn matplotlib anndata gseapy
pip install torch torchvision torchaudio
How to Run the Pipelines
1. Clone the repository
bash
Copy code
git clone https://github.com/<your-username>/Effect-of-Ageing-on-Macrophage-Transcriptomic-Profile
cd Effect-of-Ageing-on-Macrophage-Transcriptomic-Profile
2. Add datasets
Place all mouse and human data under:

kotlin
Copy code
data/
   tabula-muris-senis/
   hcla-lung/
3. Launch Jupyter
bash
Copy code
jupyter lab
4. Run notebooks
Execute notebooks in:

mouse_tabula_muris/

human_hcla/

Results & Outputs
Mouse Layer
Age-stratified DEGs

PLS-VIP age-predictive signatures

Random Forest importance scores

scVI latent embeddings

UMAP visualizations

Volcano plots & heatmaps

GO/KEGG enrichment outputs

Human Layer
Human macrophage ageing markers

ML performance metrics

Ortholog mapping

Conserved ageing signatures

Pathway-level ageing shifts

Citations
Tabula Muris Senis
Tabula Muris Consortium, Nature, 2020.

Human Cell Landscape (HCL/HCLA)
HCL Consortium, Nature, 2021.

License
This project is released under the MIT License.

yaml
Copy code

---

If you want, I can also:

✅ Add badges (Python version, license, stars)  
✅ Add a banner graphic  
✅ Add a graphical abstract  
✅ Add a “Getting Started” quickstart section  

Just tell me!











ChatGPT can make mistakes. Check important info. See Cookie Preferences.
