# High Purity Differential Expression Pattern of Genes across Spatial Domains

This repository contains the datasets and computational results supporting the three main case studies (Functional Regulation in Breast Cancer, Phenotypic Heterogeneity in Alzheimer's Disease, and Communication Niches in Tissue Neighborhoods).

## Framework

<img width="3960" height="4030" alt="2_Framework_of_HiPDEP_Analyzer" src="https://github.com/user-attachments/assets/c9a01c72-34cc-41bf-b370-68dbcc30916b" />


* **Quantification:** We formulate the Spatial Purity Index (SPi) to quantify the unilateral bias of differentially expressed genes, classifying spatial domains as Up-Regulation (UR) or Down-Regulation (DR) dominant.
* **Universality Verification:** We establish a multi-omics benchmark dataset to statistically validate HiP-DEP as a universal hallmark of spatial transcriptomics.
* **Application:** We apply the framework to decode biological contexts across three spatial domains, which correspond to the uploaded datasets: tumor regulation gradients in breast cancer, phenotypic divergence in Alzheimer's plaques, and communication niches in tissue neighborhoods.

---

## Results Data Description

### 1. Functional Regulation in Breast Cancer
**Description:** We applied the framework to ST data from a HER2-positive breast cancer tissue section, where pathologists annotated the tissue into seven spatial domains ( Adipose tissue, Breast glands, Cancer in situ, Connective tissue, Immune infiltrate, Invasive cancer, and Undetermined sites).

**Key Findings:** The analysis revealed a Tumor Regulation Gradient, where the disease core maintains high-purity expression (UR domain) that diminishes with distance, reflecting the decay of transcriptional influence.

**Data Files:**

* 切片空间域注释图像：pathologists_domain_annotation.pdf
* 空间转录组数据的空间域标签信息和位置信息：domainlabel_coords_for_spots.xlsx
* 空间转录组数据的基因表达信息：expression_count_matrix.tsv
* 单细胞参考数据：RCTD_cell_types.rds
* Seurat作为差异表达分析工具的计算结果(p-value & logFC)：Seurat_DE_result.xlsx
* DESeq2作为差异表达分析工具的计算结果(p-value & logFC)：DESeq2_DE_result.xlsx
* SPARKX作为差异表达分析工具的计算结果(p-value & logFC)：SPARKX_DE_pvalue.rds，SPARKX_DE_logFC.rds

### 2. Phenotypic Heterogeneity in Alzheimer's Disease
**Description:** We applied HiP-DEP to Slide-seq V2 data from the hippocampus of an Alzheimer’s
disease (AD) mouse model, where the pathological feature is β-amyloid (Aβ) plaque density.

**Key Findings:** HiP-DEP analysis uncovered hidden phenotypic heterogeneity between two pathologically similar plaques, where the Right plaque was an UR domain and the Left plaque was a DR domain, indicating divergent functional states.

**Data Files:**

* 空间转录组数据的位置和表达数据：expressioncount_coords.rds
* 阿尔兹海默症左右Aβ斑块的划分图：plaque_plot.png
* 阿尔兹海默症Aβ斑块病理特征密度数据：plaque_density.rds
* 总汇(Others，Right Plaque，Left Plaque)计算结果(p-value & logFC): DE_result.xlsx
* 右斑块不同密度下的计算结果(p-value & logFC)：RightPlaque_DE_result.xlsx
* 右斑块不同密度下的差异表达结果纯度变化：RightPlaque_purity.png
* 右斑块差异表达基因富集到的KEGG通路：RightPlaque_Pathway.txt
* 左斑块不同密度下的计算结果(p-value & logFC)：LeftPlaque_DE_result.xlsx
* 左斑块不同密度下的差异表达结果纯度变化：LeftPlaque_purity.png
* 左斑块差异表达基因富集到的KEGG通路：LeftPlaque_Pathway.txt

### 3. Communication Niches in Tissue Neighborhoods
**Description:** This study analyzed a 10x Visium spatial transcriptomics (ST) dataset of the human dorsolateral prefrontal cortex (DLPFC). The tissue was annotated into five distinct TCNs using CytoCommunity.

**Key Findings:** High-purity UR domains (TCN2 and TCN4) were found to spatially coincide with the tissue's most active cell-communication niches, as validated by ligand-receptor interaction analysis.

**Data Files:**

* 空间转录组数据的位置信息：coords_for_spots.txt
* 空间转录组数据的基因表达信息：expression_count_matrix.h5
* 利用CytoCommunity对细胞组织邻域的划分结果：CytoCommunity_TCNsResult.csv, CytoCommunity_TCNsResult.pdf
* Seurat作为差异表达分析工具的计算结果(p-value & logFC)：Seurat_DE_result.xlsx
* DESeq2作为差异表达分析工具的计算结果(p-value & logFC)：DESeq2_DE_result.xlsx
* SPARKX作为差异表达分析工具的计算结果(p-value & logFC)：SPARKX_DE_pvalue.rds，SPARKX_DE_logFC.rds
