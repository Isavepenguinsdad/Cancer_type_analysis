# Dose-Response Analysis of Anti-Cancer Drugs Using GDSC2 Dataset

## Overview  
This project analyzes the drug sensitivity profiles across various cancer cell lines using the publicly available GDSC2 (Genomics of Drug Sensitivity in Cancer) dataset. Unlike raw concentration-response curve analysis, this dataset contains precomputed summary metrics such as AUC and LN_IC50, which represent overall drug efficacy and cell line sensitivity. Thus, the focus is on comparing and profiling drug responses across cell lines rather than reconstructing dose-response curves.

## Data Collection  
- **Dataset Source:** GDSC2 Fitted Dose Response - Oct 27, 2023  
- **File Used:** `GDSC2_fitted_dose_response_27Oct23.xlsx`  
- **Description:** Contains model-derived summary dose-response metrics (e.g., AUC, LN_IC50) for multiple drugs tested across hundreds of cancer cell lines. Also includes annotations like cancer type (TCGA_DESC).

## Objective  
- Explore and clean the GDSC2 summarized dose-response dataset  
- Identify top drugs based on efficacy metrics like AUC  
- Profile and compare drug sensitivity across cell lines  
- Visualize response distributions and heatmaps for drug-cell line combinations  
- Prepare groundwork for downstream analyses such as machine learning prediction models

## Methods

### Data Cleaning  
- Checked for missing data with `df.isnull().sum()`  
- Imputed missing cancer type annotations (`TCGA_DESC`) with "Unknown"  
- Verified data consistency and completeness  

### Exploratory Data Analysis  
- Computed summary statistics (mean, median, std) of AUC values  
- Grouped data by drug and cell line to examine sensitivity patterns  
- Focused on top-performing drugs and cell lines for detailed visualization  

### Visualization  
- Boxplots: Show AUC distribution for top 10 drugs, excluding outliers for clarity  
- Bar charts: Highlight top 10 most frequently tested cell lines  
- Heatmaps: Visualize AUC values across drug-cell line matrix to identify response clusters  
- Scatter plots: Compare actual vs predicted AUC values from machine learning models  
- Applied axis scaling and color palettes to improve interpretability  

## Key Findings  
- Top 10 drugs exhibit variable efficacy across different cell lines  
- AUC values tend to cluster near 1.0, indicating resistance in many cell lines  
- Summarized metrics allow efficient cross-comparison without raw dose-response curves  

## Technologies Used  
- Python 3.x  
- Pandas, NumPy  
- Plotly, Dash for interactive visualization  
- Jupyter Notebook  

## Next Steps  
- Incorporate IC50 and other potency metrics for deeper insight  
- Add cancer type–specific analysis using `TCGA_DESC` annotations  
- Expand interactive dashboard features  
- Explore clustering and machine learning to predict drug responses  

> **Note:** This project is still evolving. Enhancements such as interactive dashboards and additional analyses are planned in future iterations.

