# anti-EGFR-ADC
R scripts to investigate TNBC transcriptomic data using publicly available datasets: scRNA-seq (GSE161529) and spatial transcriptomics (GSE210616).

# Figure 2AB, S2A, S3A
A script to visualize clusters and gene expression across breast cancer subtypes (TNBC, HER2+ nd ER+), using publicly available data from "A single-cell RNA expression atlas of normal, preneoplastic and tumorigenic states in the human breast", DOI 10.15252/embj.2020107333 


Data is downloaded as pre-processed Seurat objects from:
figshare: https://figshare.com/articles/dataset/Data_R_code_and_output_Seurat_Objects_for_single_cell_RNA-seq_analysis_of_human_breast_tissues/17058077 

Files used in the downstream analysis:  
- SeuratObject_TNBC.rds
- SeuratObject_HER2.rds
- SeuratObject_ERTotal.rds

Seurat objects are used as provided by the authors of the original manuscript. Our analysis involves visualization of gene expression and visualization of non-zero counts of genes of interest across BC subtypes. Figures are present in Figure 2 and Supplementary Figure 2 and 3.

# Figure 2C 
A script to project and retrieve gene expression from publicly available breast cancer spatial transcriptomics data from "Spatial Transcriptomic Analysis of a Diverse Patient Cohort Reveals a Conserved Architecture in Triple-Negative Breast Cancer", doi: 10.1158/0008-5472.CAN-22-2682 .

The analysis focuses on showing gene expression on an example of treatment naive and post-treatment BC slices, followed by analysis of gene co-occurence within a spot. Tissue slices 117B and 117D are used for the gene visualization analysis, while all slices are used to calculate the co-occurence.

The original data is available as GSE210616. The image information had to be corrected as the submission of image files was incorrect. In the `scalefactors_json.json` file, the value for "tissue_lowres_scalef" had to be replaced by the value in "tissue_hires_scalef" to allign the spots coordinates with the re-scaled image.
