# High Purity Differential Expression Pattern of Genes across Spatial Domains

This repository contains the results data for the study on High-Purity Differential Expression (HiP-DEP) patterns across spatial domains.

## Framework

![2_Framework_of_HiPDEP_Analyzer](../fig/2_Framework_of_HiPDEP_Analyzer.png)

* **Quantification:** We formulate the Spatial Purity Index (SPi) to quantify the unilateral bias of differentially expressed genes, classifying spatial domains as Up-Regulation (UR) or Down-Regulation (DR) dominant.
* **Universality Verification:** We establish a multi-omics benchmark dataset to statistically validate HiP-DEP as a universal hallmark of spatial transcriptomics.
* **Application:** We apply the framework to decode biological contexts across three spatial domains, which correspond to the uploaded datasets: tumor regulation gradients in breast cancer, phenotypic divergence in Alzheimer's plaques, and communication niches in tissue neighborhoods.

---

## Results Data Description

### 1. Breast Cancer Spatial Transcriptomics Data (Slice H)
**Description:** This study applied the framework to ST data from a HER2-positive breast cancer tissue section, where pathologists annotated the tissue into seven spatial domains (e.g., Invasive cancer, Cancer in situ) based on HE images.

**Key Findings:** The analysis revealed a Tumor Regulation Gradient, where the disease core maintains high-purity expression (UR domain) that diminishes with distance, reflecting the decay of transcriptional influence.

**Data Files:**

* `spot_label.xlsx`: 空间转录组数据的空间域标签信息
* `spot_count.tsv`: 空间转录组数据的表达信息
* `RCTD_cell_types.rds`: 单细胞参考数据
* `H1_annotation.jpg`: 切片空间域注释图像
* `wilcox_DE_res.xlsx`: wilcox差异表达分析结果
* `DESeq2_DE_res.xlsx`: DESeq2差异表达分析结果
* `genes_sig_SPARKX.rds`: SPARKX差异表达结果的p-value
* `logFC_SPARKX.rds`: 差异表达结果的logFC

### 2. Alzheimer's Disease Spatial Transcriptomics Data
**Description:** This dataset examines the relationship between Aβ plaque density and differential gene expression patterns in the hippocampal region of an Alzheimer's disease mouse model.

**Key Findings:** HiP-DEP analysis uncovered hidden phenotypic heterogeneity between two pathologically similar plaques, where the Right plaque was an UR domain and the Left plaque was a DR domain, indicating divergent functional states.

**Data Files:**
* `counts_coords.rds`: 空间转录组数据的位置和表达数据
* `plaque_density.rds`: 阿尔兹海默症Aβ斑块病理特征密度数据
* `plaque_plot.png`: 阿尔兹海默症左右Aβ斑块的划分图
* `DE_res.xlsx`: 阿尔兹海默症两个Aβ斑块的差异表达分析结果
* `RightPlaque_Pathway.txt`: 右斑块差异表达基因富集到的KEGG通路
* `RightPlaque_DE_result.xlsx`: 右斑块不同密度下的差异表达结果
* `RightPlaque_purity.png`: 右斑块不同密度下的差异表达结果纯度变化
* `LeftPlaque_Pathway.txt`: 左斑块差异表达基因富集到的KEGG通路
* `LeftPlaque_DE_result.xlsx`: 左斑块不同密度下的差异表达结果
* `LeftPlaque_purity.png`: 左斑块不同密度下的差异表达结果纯度变化

### 3. DLPFC-151670 Slice (Tissue Cellular Neighborhoods)
**Description:** This study analyzed tissue cellular neighborhoods (TCNs) in the human dorsolateral prefrontal cortex (DLPFC) to investigate whether HiP-DEP patterns correspond to functional niches.

**Key Findings:** High-purity UR domains (TCN2 and TCN4) were found to spatially coincide with the tissue's most active cell-communication niches, as validated by ligand-receptor interaction analysis.

**Data Files:**

* `DLPFC-151670_Coordinates.txt`: 空间转录组数据的spot位置信息
* `matrix.h5`: 空间转录组数据的表达信息
* `ResultTable_DLPFC-151670.csv`: 利用CytoCommunity对细胞组织邻域的划分结果
* `TCN_DLPFC-151670.pdf`: 细胞组织邻域的划分结果
* `wilcox_DE_res.xlsx`: wilcox差异表达分析结果
* `DESeq2_DE_res.xlsx`: DESeq2差异表达分析结果
* `genes_sig_SPARKX_TCNs.rds`: SPARKX差异表达结果中的p-value结果
* `logFC_SPARKX_TCNs.rds`: 差异表达结果中的logFC结果