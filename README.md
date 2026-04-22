AI Job Trends Analysis: Impact of AI on Employment, Salaries, and Workforce Dynamics
Project Overview

This project analyzes the impact of Artificial Intelligence (AI) on the job market across industries. The objective is to understand how AI influences job demand, salary structures, automation risk, and workforce composition, and to derive actionable insights for decision-making.

The analysis follows an end-to-end data pipeline, including data extraction, cleaning, exploratory data analysis (EDA), statistical analysis, and dashboard development.

Problem Statement

The rapid adoption of AI is transforming the global job market. Organizations face challenges in:

Identifying future high-growth roles
Understanding salary drivers in AI-influenced jobs
Managing automation risk across job categories
Designing workforce strategies aligned with future demand

This project aims to answer these challenges through data-driven analysis.

Dataset Description
Source: AI Job Trends Dataset
Size: ~30,000 rows, 13 columns
Type: Tabular dataset with job-level records
Key Features:
Job Title
Industry
Job Openings (2024, 2030)
Median Salary (USD)
AI Impact Level
Automation Risk (%)
Required Education
Required Experience
Remote Work Ratio (%)

Project Structure
SectionName_TeamID_ProjectName/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   └── ai_job_trends_dataset.csv
│   └── processed/
│       └── cleaned_jobs.csv
│
├── notebooks/
│   ├── 01_extraction.ipynb
│   ├── 02_cleaning.ipynb
│   ├── 03_eda.ipynb
│   ├── 04_statistical_analysis.ipynb
│   └── 05_final_load_prep.ipynb
│
├── scripts/
│   └── etl_pipeline.py
│
├── tableau/
│   ├── screenshots/
│   └── dashboard_links.md
│
├── reports/
│   ├── project_report.pdf
│   └── presentation.pdf
│
└── docs/
    └── data_dictionary.md

Methodology
1. Data Extraction
Dataset loaded using Python (Pandas)
Initial inspection of structure, types, and missing values
2. Data Cleaning and Transformation
Standardization of column names
Handling missing values
Data type corrections
Outlier detection and treatment
Feature engineering:
Growth Rate
Automation Risk Categories
3. Exploratory Data Analysis (EDA)

EDA is structured into four key areas:

1. Job Growth and Demand
Growth rate distribution
Industry-wise growth comparison
Identification of top growing and declining roles
Relationship between AI impact and growth
2. Salary Analysis
Salary distribution
Salary variation across industries
Impact of experience and education
Relationship between AI impact and salary
3. Automation Risk
Distribution of automation risk
Risk vs job status
Risk vs growth relationship
Risk segmentation
4. Workforce Structure
Education and experience distribution
Remote work trends
Impact of remote work on salary and growth
4. Statistical Analysis (In Progress)

Planned analysis includes:

Correlation analysis
Hypothesis testing (t-tests, ANOVA)
Regression modeling:
Salary drivers
Growth drivers
5. Dashboard Development (Planned)

The Tableau dashboard will include four main views:

Job Growth and Future Demand
Salary Drivers and AI Impact
Automation Risk Analysis
Workforce Trends and Hiring Strategy

Each dashboard is designed to answer specific business questions and support decision-making.

Current Status
Data extraction and cleaning: Completed
Exploratory Data Analysis: Completed (under refinement)
Statistical analysis: In progress
Dashboard development: Pending
Key Insights (Preliminary)
AI-driven roles show significantly higher growth rates
High AI impact roles command higher salaries
Jobs with high automation risk are more likely to decline
Mid-level experience roles dominate job demand
Remote work is associated with competitive salary trends
Tools and Technologies
Python (Pandas, NumPy, Matplotlib, Seaborn)
Jupyter Notebook / Google Colab
Tableau Public
GitHub for version control
Next Steps
Finalize statistical analysis with hypothesis testing and regression
Build Tableau dashboards with interactive filters
Generate business recommendations based on insights
Complete final report and presentation
Notes

This README reflects the current progress of the project and will be updated as further analysis and dashboard development are completed.
