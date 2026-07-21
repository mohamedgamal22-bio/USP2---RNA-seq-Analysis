This repository contains a complete bulk RNA-seq analysis pipeline performed on publicly available sequencing data

The goal of this study is to compare gene expression profiles between:

- Empty vector control cells
- USP2 overexpression cells

The analysis starts from raw FASTQ sequencing reads and ends with differential gene expression analysis and data visualization.

---

 Workflow

The following analysis pipeline was performed:

1. Download raw sequencing data from NCBI SRA
2. Quality control using FastQC
3. Read alignment to the human genome using HISAT2
4. Gene quantification using featureCounts
5. Differential expression analysis using DESeq2
6. Data visualization including:
   - PCA
   - Volcano Plot
   - Sample Distance Heatmap

---

 Repository Structure

```
.
├── code.txt                # R analysis script
├── metadata.lung.txt       # Sample metadata
├── clean_count.txt         # Gene count matrix
├── Heatmap.png             # Sample distance heatmap
├── PCA.png                 # PCA plot
├── Volcano.png             # Volcano plot
├── empty_two.1_fastqc.html # FastQC report
└── README.md
```

---

 Experimental Design

| Group | Description |
|--------|-------------|
| Empty Vector | Control cells |
| USP2 Overexpression | Cells overexpressing USP2 |

Three biological replicates were analyzed for each condition.



 Differential Expression Analysis

Differential expression analysis was performed using DESeq2.

Because of the limited number of biological replicates (3 vs 3), no genes passed the Benjamini-Hochberg false discovery rate threshold (adjusted p-value < 0.05).

Exploratory visualizations were therefore generated using nominal (uncorrected) p-values.



 Tools Used

- FastQC
- HISAT2
- featureCounts
- DESeq2
- EnhancedVolcano
- ggplot2
- R



 Learning Objectives

This project was completed as a practical exercise to learn a complete RNA-seq analysis workflow, including:

- Processing raw sequencing reads
- Read alignment
- Gene counting
- Differential expression analysis
- Statistical interpretation
- Biological data visualization
