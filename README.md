# **RNA‑seq Differential Expression Analysis — GSE60424 — README**

## **Overview**

This repository contains a full RNA‑seq differential expression analysis of **GSE60424**, comparing **human neutrophils** vs **whole blood**.
The project uses **pydeseq2** for DESeq2‑style modelling and **gseapy** for GO, KEGG, and Reactome enrichment analysis.

## **Dataset**

- GEO Accession: **GSE60424**
- Organism: *Homo sapiens*
- Conditions: Neutrophils vs Whole Blood
- Platform: Illumina HiSeq
- Samples: 12

## **Workflow**

### **1. Data Preparation**

- Load raw count matrix
- Load metadata
- Align samples
- Filter low‑count genes

### **2. Normalisation**

- Size‑factor estimation
- Variance stabilising transformation (VST)
- PCA for QC

### **3. Differential Expression**

- Wald test
- Log2 fold change shrinkage
- Volcano and MA plots
- Export results table

### **4. GSEA (Preranked)**

Rank metric:

score=log2FC⋅−log⁡10(p)

Analyses performed:

- GO Biological Process
- KEGG 2021 Human
- Reactome 2022

### **5. Key Findings**

- Strong enrichment for **neutrophil degranulation**
- Upregulation of **CXCL8, S100A8, S100A9, LCN2**
- Activation of innate immune pathways
- Downregulation of erythrocyte/platelet transcripts

## **Outputs**

- `RNAseq_GSE60424.ipynb` — full analysis notebook
- Volcano plot
- MA plot
- GSEA rank file (`.rnk`)
- GO/KEGG/Reactome enrichment tables
- Enrichment plots

## **Skills Demonstrated**

- RNA‑seq analysis
- DESeq2 modelling in Python
- Gene set enrichment analysis
- Immunology and innate immune biology
- Reproducible computational workflows
