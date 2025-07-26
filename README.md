Dose-Response Analysis of Anti-Cancer Drugs Using GDSC2 Dataset
Overview
This project analyzes the dose-response relationships of anti-cancer drugs using the publicly available GDSC2 (Genomics of Drug Sensitivity in Cancer) dataset. The goal is to identify drugs that demonstrate the strongest responses across various cancer cell lines based on metrics such as AUC (Area Under the Curve). The project workflow includes data cleaning, exploratory data analysis, and visualization using Python (Pandas, Seaborn, Matplotlib).
Data Collection
•	Dataset Source: GDSC2 Fitted Dose Response - Oct 27, 2023
•	File Used: GDSC2_fitted_dose_response_27Oct23.xlsx
•	Description: The dataset contains dose-response curves (AUC, IC50) for multiple drugs tested across hundreds of cancer cell lines, along with cancer type annotations (TCGA_DESC).
Objective
•	Clean and explore the GDSC2 dataset
•	Identify top-performing drugs based on average AUC
•	Visualize drug response distributions
•	Systematically handle missing data
Methods
Data Cleaning
•	Checked for missing values using df.isnull().sum()
•	Replaced missing TCGA_DESC values with "Unknown" using fillna()
•	Verified changes with .value_counts()
Exploratory Analysis
•	Calculated summary statistics for AUC (mean, max, median, std)
•	Grouped data by DRUG_NAME and CELL_LINE_NAME to compare drug efficacy
Visualization
•	Boxplots: Displayed AUC distributions for the top 10 drugs with distinct colors per drug. Outliers were excluded to improve interpretability.
•	Histograms: Focused on AUC values greater than 0.85, highlighting concentrations of high-response data. Kernel Density Estimation (KDE) was overlaid for smoother density visualization.
•	Axis Scaling: Applied logarithmic scale to the Y-axis in boxplots to address skewness and spread values clustered near 1.
•	Layout and Readability: Utilized tight layout and rotated x-axis labels to prevent overlap and enhance clarity.
•	Color Palette: Used Seaborn’s "Set2" palette for consistent and visually appealing color coding.
Key Findings
•	The top 10 drugs (by average AUC) showed significant variability in efficacy across cell lines.
•	Many AUC values cluster near 1.0, indicating high resistance or limited response in some cases.
•	Data normalization and tailored plotting techniques were necessary to reveal subtle differences.
Technologies Used
•	Python 3.x
•	Jupyter Notebook
•	Pandas
•	Seaborn
•	matplotlib
Next Steps
•	Incorporate IC50 analysis for potency comparison
•	Add interactive visualizations using Plotly or Dash
•	Compare drug responses across different cancer types (TCGA_DESC) 
** Note: This project is still evolving. Enhancements such as interactive dashboards and additional analyses are planned in future iterations.
