# ALS-Transcriptome-Pipeline
This project presents a reproducible R-based transcriptome analysis pipeline for ALS (GSE112680) in Google Colab. Includes QC, normalization, differential expression (limma) with DEG filtering, PCA, visualization, and GO/KEGG enrichment. Fully parameterized for flexible and reproducible analysis.

This project was developed as part of the EgCompBio Diploma in Bioinformatics , focusing on applying programming skills to real-world bioinformatics problems.


**Dataset**

Source: GEO (GSE112680)

Type: Microarray (Expression profiling by array)

Samples: ALS vs healthy controls

Tissue: Whole blood

Platform: HT12_V4


**Pipeline-design-key-features**

1)Accepts expression matrix and metadata as inputs

2)Flexible group selection (case vs control)

3)Customizable thresholds (adjusted p-value, logFC)

4)Reusable across different transcriptomic datasets

5)Generates complete analysis outputs automatically


**Pipeline Workflow**

1. Data Preprocessing & Quality Control

Detection p-value filtering

Log2 transformation

Normalization

Removal of zero-variance genes

2. Metadata Processing

Alignment of expression data with metadata

Selection of ALS vs control groups

**3.Core Analysis Functions**

Function 1: Transcriptome Analysis Pipeline

Performs end-to-end analysis including:

Differential Expression Analysis

Implemented using limma

DEGs filtered using:

Adjusted p-value (FDR cutoff)

Log2 fold change threshold

Exploratory Analysis

Principal Component Analysis (PCA)

Visualization using ggplot2

Visualization

Volcano plots

Heatmaps (top variable genes / top DEGs)

Functional Enrichment

Probe ID → Entrez gene mapping

Gene Ontology (GO) analysis (gene function annotation)

KEGG pathway enrichment analysis

   Function 2: Visualization Utility
   
Loads and displays saved .png figures directly in Google Colab

Used for quick visualization of pipeline outputs


**Inputs**

Expression matrix (processed or raw QCed data)

Metadata file (sample annotations)


**Outputs**

From Pipeline Function:

Differential expression results (DEGs)

PCA plots

Volcano plots

Heatmaps

GO enrichment results

KEGG pathway enrichment results

Saved figures (.png)

From Visualization Function:

Display of generated .png plots in Colab


**Tools & Environment**

R: limma, ggplot2, clusterProfiler, ComplexHeatmap

Google Colab: R runtime environment for cloud-based execution

Methods: Bioinformatics and statistical transcriptomic analysis workflow


**Future Work**

-Integration of machine learning models for ALS classification and prediction

-Extension of the pipeline to RNA-seq datasets for broader applicability

-Enhanced biomarker discovery using advanced statistical and computational approaches


**Notes**

-Analysis focuses on ALS vs healthy controls only

-Pipeline is designed to be dataset-independent and reusable
