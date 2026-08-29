# Quantum Machine Learning for Genomic Feature Selection

This repository provides a computational framework evaluating Quantum Machine Learning (QML) against classical machine learning baselines for genomic feature selection and tissue-state classification in spatial transcriptomics (**GSE241124**). 

Developed as an undergraduate research thesis at the Lebanese University, the project benchmarks classical dimensionality reduction techniques against hybrid NISQ-era quantum architectures to isolate synergistic gene-gene interactions in wound healing datasets.

---

## Features

* **Hybrid Quantum Architectures**: Implements a 15-qubit Variational Quantum Feature Selection (VQFS) network integrated with Complementary Pairs Stability Selection (CPSS) alongside Projected Quantum Kernel Support Vector Machines (Q-SVM).
* **Classical Baselines**: Includes baseline implementations of Principal Component Analysis (PCA), Sparse PCA, Independent Component Analysis (ICA), and Variational Autoencoders (VAE) for comparative feature selection.
* **Leakage-Free Evaluation**: Utilizes donor-grouped nested cross-validation to prevent data leakage across spatial transcriptomics donor replicates.
* **Biological Interpretability**: Integrates Gene Ontology (GO) functional enrichment mapping to evaluate the biological significance of quantum-selected gene sub-sets.

---

## Tech Stack 

| Category | Tools & Libraries |
| :--- | :--- |
| **Quantum Computing** | Qiskit, PennyLane |
| **Machine Learning** | PyTorch, Scikit-Learn |
| **Bioinformatics** | Scanpy, AnnData, GSEAPY |
| **Data Processing** | NumPy, Pandas, SciPy |

---

## Pipeline Architecture

```text
Raw Spatial Transcriptomics (GSE241124)
           │
           ▼
 Scanpy Quality Control & Filtering
           │
   ┌───────┴───────────────────────────┐
   ▼                                   ▼
Classical Baselines         Quantum Architectures  
   │                                   │
   │                                   │
   └───────┬───────────────────────────┘
           ▼
  Donor-Grouped Nested CV
           │
           ▼
 MLFlow Experimental Tracking
           │
           ▼
 GO Functional Enrichment Mapping
```

---

## Repository Structure

├── data/ 
├── preprocessing/
├── models/ 
├── requirements.txt 
└── README.md

---

## Installation

```bash
git clone https://github.com/batoul-hamieh/QML_Genomic_Feature_Selection.git
cd QML_Genomic_Feature_Selection
```
```bash
python -m venv venv
source venv\Scripts\activate
pip install -r requirements.txt
```
---
