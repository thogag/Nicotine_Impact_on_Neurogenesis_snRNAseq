# Nicotine_scRNAseq_Neurodevelopment

## Project overview
This project investigates the impact of **nicotine exposure** on **neuronal development** using **single-cell RNA sequencing (scRNA-seq)** data.

By combining:
- multi-resolution clustering,
- neuronal subtype annotation,
- differential gene expression,
- pathway enrichment analysis (GSEA),
- and pseudotime trajectory inference,

we aim to identify how nicotine alters neuronal states, developmental progression, and key biological pathways.
In the long term, the goal is to copy this process performed on neurons, on all other cell types of the dataset. To know that this dataset is public and has been retrieved on [Kaggle](https://www.kaggle.com/datasets/alexandervc/scrnaseq-human-embryonic-stem-cell-under-nicotine) and whose reference paper is:
[Single-Cell RNA Sequencing of Human Embryonic Stem Cell Differentiation Delineates Adverse Effects of Nicotine on Embryonic Development](https://pmc.ncbi.nlm.nih.gov/articles/PMC6449785/)


---

## Biological question
How does nicotine exposure affect:
- neuronal subtype composition?
- developmental trajectories?
- metabolic and stress-related pathways during neurogenesis?

---

## Dataset & experimental design
- **scRNA-seq dataset** including multiple cell types
- Two conditions:
  - **N**: Nicotine-exposed
  - **D**: Control
- Focused downstream analysis on **neuronal populations**

---

## Analysis workflow

### 1. Global dataset analysis
- Quality control & normalization
- Cell-type identification
- UMAP visualization of all cell populations

### 2. Neuronal analysis — resolution 0.4
- Identification of major neuronal states
- Marker-based annotation:
  - Neuroepithelial stem cells
  - Pluripotent / stem-like cells
  - Neural progenitors
  - Differentiating neurons
- Differential expression (N vs D)
- Pathway enrichment (Hallmark GSEA)

### 3️. Neuronal refinement — resolution 0.7
- Identification of finer neuronal subtypes
- Sensory neuron-like populations
- Eye-field / forebrain progenitors
- Cluster proportion comparison between conditions

### 4. Trajectory inference
- Pseudotime analysis using **Slingshot**
- Neurodevelopmental trajectory starting from neuroepithelial stem cells
- Comparison of pseudotime distributions between N and D
- Gene expression dynamics along pseudotime (e.g. *SOX11, EPCAM, UBE2C*)

---

## Key results
- Nicotine exposure is associated with:
  - enrichment of **MYC targets**, **E2F targets**, and **oxidative phosphorylation**
  - altered ROS-related pathways
  - shifts in neuronal developmental trajectories
- Control cells show relative enrichment of stress- and hypoxia-related signatures
- Pseudotime analysis suggests nicotine may **accelerate neuronal differentiation**

---

## Biological interpretation
These results support a model in which nicotine:
- enhances proliferative and metabolic programs,
- perturbs redox homeostasis,
- and biases neural progenitors toward accelerated differentiation,
potentially at the cost of proper maturation and cellular homeostasis.

---

## Tools & packages
- **R at 4.5.0**
  - Seurat (5.4.0)
  - Slingshot (2.18.0)
  - clusterProfiler (4.18.4)
  - msigdbr (25.1.1)
  - ggplot2 (4.0.1)

---

## What's remain for neurons?
- Further validation of key gene expression changes
- Integration with additional datasets or modalities
- Functional assays to assess neuronal maturation and function
- Exploration of long-term effects of nicotine on neuronal populations

## Whats' remain for the project?
- Extend analysis to other cell types in the dataset
- Comparative analysis with other neurotoxic exposures
- Integration with spatial transcriptomics data if available
- Manuscript preparation and dissemination of findings

---

## Contact

If you have questions or would like to discuss the analysis, feel free to open an issue or reach out.

