# Inhibitors_pIC_RNA-seq
_Bulk RNA-seq analysis for A549 cells treated with inhibitors, then stimulated with pIC_\
Scripts associated with the bulk RNA-seq data for the unstimulated clones in Single-cell heterogeneity in interferon induction potential is heritable and governed by variation in cell state, Thayer et al. (2025).
## Overview
This repository contains the .Rmd script used to analyze the bulk RNA-seq data collected from A549 cells. 
These cells were treated with either DMSO, JNK-IN-8, ruxolitinib, or both inhibitors, then either kept unstimulated or stimulated with pIC. 
The RNA was collected 16 hours post transfection with pIC then taken for bulk RNA-seq. 
The processing of the raw files is almost exactly the same as what has already been posted in https://github.com/BROOKELAB/Clones_RNA-seq. 

The goal of this analysis is to see how JNK-IN-8 treatment affects the _IFNL1_ response to pIC the transcriptional level. 
We added ruxolitinib treatment to the experiment to also control for any secondary signaling that may be taking place from the JAK/STAT pathway.

## Analysis in R
### Script: eto2b21.48_12.8.25.Rmd
This script performs:\
:white_check_mark: Loads the count matrix and creates an edgeR object for DE analysis\
:white_check_mark: Creates a PCA plot to look at the transcriptional similarity of the different experimental conditions\
:white_check_mark: Creates multiple design matrices and QLF tests to look at the DE of specific conditions (comp1-11)\
:white_check_mark: Creates a heatmap of the expressions of specific genes of interest

### Requirements
**R (v4.2.2)**
- org.Hs.eg.db (v3.16.0)
- edgeR (v3.40.2)
- dplyr (v1.1.4)
- tidyr (v1.3.1)
- ggplot2 (v3.5.1)
- gtools (v3.9.5)
- ComplexHeatmap (v2.14.0)
- circlize (v0.4.16)
- forcats (v1.0.0)
- tibble (v3.2.1)
