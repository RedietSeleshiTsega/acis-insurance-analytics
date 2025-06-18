ACIS Car Insurance Analytics
Project Overview
This repository contains the code and documentation for a data analytics project conducted for AlphaCare Insurance Solutions (ACIS) to optimize car insurance pricing and marketing strategies in South Africa. The project leverages historical claim data (February 2014–August 2015) to uncover risk and profitability patterns, validate key hypotheses, and build predictive models for claim severity, premium optimization, and claim probability. The analysis supports ACIS’s goal of targeting low-risk customer segments and refining pricing strategies.
Objectives

Exploratory Data Analysis (EDA): Understand distributions, trends, and relationships in the dataset to identify risk and profitability drivers.
Data Versioning: Implement Data Version Control (DVC) to ensure reproducibility and regulatory compliance.
Hypothesis Testing: Validate risk and margin differences across provinces, postal codes, and genders.
Predictive Modeling: Develop machine learning models to predict claim amounts, optimal premiums, and claim likelihood.
Recommendations: Provide data-driven strategies for pricing adjustments and targeted marketing.

Repository Structure
acis-insurance-analytics/
├── data/
│   └── MachineLearningRating_v3.txt.dvc 
├── .dvc/                               
├── .gitignore    
├── notebooks/
│   └── eda_analysis.ipynb 
│   └── hypothesis_testing.ipynb 
│   └── modeling.ipynb                                            
├── README.md                            
└── requirements.txt                     

Setup Instructions
To reproduce the analysis, follow these steps:

Clone the Repository:
git clone https://github.com/RedietSeleshiTsega/acis-insurance-analytics
cd acis-insurance-analytics


Set Up a Virtual Environment:
py -m venv venv
venv/bin/activate 


Install Dependencies:
pip install -r requirements.txt

Dependencies include:
pandas==1.5.3
numpy==1.23.5
matplotlib==3.7.1
seaborn==0.12.2
dvc==3.55.2
scikit-learn==1.2.2
xgboost==2.0.3
statsmodels==0.14.0


Set Up DVC:

Initialize DVC (if not already done):dvc init


Configure local storage:mkdir C:\Users\bless\OneDrive\Desktop\dvc_storage
dvc remote add -d localstorage C:/Users/bless/OneDrive/Desktop/dvc_storage


Pull the dataset:dvc pull data/MachineLearningRating_v3.txt.dvc

Note: The dataset (MachineLearningRating_v3.txt) is not stored in Git but tracked via DVC. Contact the project team for access if needed.


Run Notebooks:

Open Jupyter Notebook:jupyter notebook


Execute eda_analysis.ipynb, hypothesis_testing.ipynb, and modeling.ipynb in order.



Usage

EDA (eda_analysis.ipynb): Generates visualizations (e.g., loss ratio by province, claim distribution) saved as PNG files.
Hypothesis Testing (hypothesis_testing.ipynb): Tests hypotheses about risk and margin differences, outputting p-values and interpretations.
Modeling (modeling.ipynb): Builds and evaluates Linear Regression, Random Forest, and XGBoost models for claim severity, premium prediction, and claim probability.
Final Report (insurance_analytics_report.md): Summarizes findings and recommendations in a business-friendly format.

Key Deliverables

Visualizations: Loss ratio by province, claim distribution with outliers, and premium vs. claims by gender (saved as *.png).
Statistical Insights: Rejected hypotheses indicate significant risk differences across provinces and postal codes, guiding regional pricing.
Predictive Models: XGBoost models for claim severity and premium prediction, with Random Forest for claim probability.
Recommendations:
Adjust premiums by 10–15% in high-risk provinces (e.g., Gauteng).
Target newer vehicles and low-risk postal codes for marketing.
Deploy predictive models for dynamic pricing.



Notes

Data Access: The dataset (MachineLearningRating_v3.txt) is managed via DVC and stored in C:/Users/bless/OneDrive/Desktop/dvc_storage. Contact the team for access.
Git Workflow: The project uses branches (task-1, task-2, task-3, task-4) with Pull Requests merged into main.
Submission: Final deliverables were submitted on June 18, 2025, for review by facilitators Mahlet, Kerod, Rediet, and Rehmet.

Contributors

Rediet Seleshi, Marketing Analytics Engineer

Contact
For questions or data access, contact the ACIS data analytics team or the project facilitators.

Submission Date: June 18, 2025 GC
