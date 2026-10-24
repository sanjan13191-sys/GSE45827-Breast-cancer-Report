# Final Bioinformatics Report - GSE45827 Breast Cancer

## 1. Research Question
What are the differentially expressed genes between breast cancer subtypes (Basal, HER2, Luminal A, Luminal B) and normal tissues, and what pathways do they represent?

## 2. Methods
**Dataset:** GSE45827 from NCBI GEO - 155 samples (130 breast tumor, 25 normal)
- Platform: Affymetrix Human Genome U133 Plus 2.0
- Source: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE45827

**Workflow:**
1. **Data Curation (Task 2):** Downloaded raw data, checked sample count (155), removed ambiguous probes, cleaned data structure. File: GSE45827_data.csv
2. **Data Summarization:** Calculated sample groups, mean expression per subtype.
3. **Visualization (Task 3):**
      - Boxplot: To check data normalization and quality across 155 samples
      - Volcano Plot: log2FoldChange vs -log10(p-value) to identify significant genes (cutoff: |log2FC|>1, p<0.05)
      - Heatmap: Top 50 significant genes across subtypes

**Tools Used:** GEO2R, Python (pandas), R (limma concept), Excel for curation

## 3. Results
- **Samples Processed:** 155 samples curated successfully
- **Significant Genes:** ~ 250 genes passed filter (log2FC >1 and p<0.05)
    - Upregulated examples: MKI67, ERBB2 (HER2), FOXC1 (Basal marker)
    - Downregulated: Normal breast markers
- **Visualizations:**
    - Boxplot showed proper normalization
    - Volcano plot separated significant genes (red dots)
    - Heatmap showed distinct clustering: Basal vs Luminal A vs HER2
- **Biological Insight:** Basal subtype shows high proliferation genes, Luminal A shows ER-related genes

## 4. Limitations
1.  Microarray data only - not RNA-seq, limited sensitivity
2.  Single dataset analysis - needs validation in TCGA or other cohort
3.  Remote / In-silico only - no wet-lab validation (qPCR, IHC)
4.  No clinical survival correlation done
5.  Pathway analysis is predicted, not experimentally confirmed

## 5. References
1. Prat et al. - GSE45827 dataset - NCBI GEO
2. Perou et al. (2000) Molecular portraits of human breast tumours - Nature
3. NCBI GEO Database: GSE45827
4. SWYNEX Bioinformatics Internship Tasks 1-3

## Files in Repo
- GSE45827_data.csv (curated data)
- Boxplot.png
- Volcano_plot.png
- Heatmap.png
- Final_Report.pdf (this file as PDF)

**Author:** Sanjana D - M.Sc Biotechnology, Mangalore University | Bioinformatics Intern @ SWYNEX
**Date:** October 2026
**Purpose:** Task 4 Final Report + CodeSlice Interview Preparation
