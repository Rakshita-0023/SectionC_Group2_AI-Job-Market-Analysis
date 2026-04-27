AI Job Trends: Growth, Salary & Automation Risk (2024–2030)
Sector: Future of Work / Labor Market Analytics / AI & Automation

Prepared by Group 2:

Name	
Aabir Sarkar	
Abhiman Singh	
Aparna Singh
Ayush Kumar
LAKSHYA YADAV
Polana Rakshita
Saumya Mishra


Institute: Rishihood University (NST)

Course / Project: [Add course name]

Faculty / Mentor: [Add name]

Executive Summary
This project analyzes how AI adoption and automation are reshaping job markets across industries, focusing on job growth projections (to 2030), salary drivers, and automation risk. Using a structured dataset of job roles and industry attributes, we built an end-to-end Python pipeline to clean data, compute business KPIs, perform exploratory data analysis (EDA), and run statistical tests and regression models.

What We Did
We organized the analysis into four themes:

Job Growth & Future Demand — distribution of growth rates, industry-level growth, and identification of top growing/declining jobs.
Salary Drivers & AI Impact — salary distribution, salary differences by industry and AI impact, and the role of experience/education/remote work.
Automation Risk — distribution of automation risk and its relationship with job decline and growth.
Workforce Structure — education demand, experience distribution, and remote-work patterns.
What We Found (High-Level)
AI-driven growth: Roles with higher AI exposure/AI impact tend to show stronger growth potential, signaling a workforce shift toward AI-centric skills.
Salary stratification: Salaries are strongly shaped by industry + experience + education + AI impact, with clear stratification across sectors.
Automation vulnerability: Automation risk is associated with job vulnerability—roles more exposed to automation are more likely to be declining.
Remote work premium: Remote-enabled roles often show higher salary patterns, especially in tech-driven domains.
Why It Matters (Business Value)
The results help decision-makers (employers, policy teams, educators) prioritize:

Where to invest in hiring (high-growth industries/roles)
Which roles need reskilling pathways (high-risk declining roles)
What drives compensation (experience, education, remote work, AI impact)
Deliverables
A cleaned and aggregated dataset ready for Tableau
KPI framework (jobs, salary, growth, risk, status distributions)
EDA + statistical validation (correlation, hypothesis tests, regressions)
Dashboard blueprint (growth, salary, risk, workforce)
Sector Context and Problem Statement
Sector Context: AI, Automation, and Labor Markets
Organizations face uncertainty in workforce planning as AI tools and automation technologies rapidly change:

Which industries will expand employment demand (new job creation)
Which job families will shrink (task automation and process digitization)
How compensation will evolve (premium for AI-related skills)
How education and experience translate into employability and pay
Which roles are most exposed to automation risk
This makes workforce strategy increasingly data-driven: hiring plans, training budgets, university curricula, and policy interventions need evidence rather than assumptions.

Problem Statement
The project addresses the following decision problem:

How can we quantify and explain job growth, salary patterns, and job vulnerability (automation risk) across industries, and determine whether AI impact measurably affects growth and pay?

Business Questions (Mapped to the Work)
Growth & Demand
Which industries are projected to grow the most by 2030?
Which job roles are declining?
How does AI impact relate to growth?
Salary
Do AI-heavy roles pay more?
How does experience affect salary?
Which industries offer the highest pay?
Risk
Which jobs are most at risk from automation?
Do high-risk jobs decline more?
Which industries are safer?
Workforce
What education levels are most valuable?
Does remote work influence salary and growth?
How does experience affect growth potential?
Data Description — Source, Structure, Size, and Limitations
Data Source
Dataset: AI Job Trends / Future-of-work job role dataset (as provided for the project).

[Note: Add the exact source link or platform: Kaggle / course-provided / internal dataset, etc.]

Structure (Typical Columns Used)
The dataset contains the following key analytical dimensions:

Job Role / Job Title (categorical)
Industry (categorical)
Job Status (categorical; e.g., increasing/declining/stable)
Growth Rate (numeric; 2024→2030 projection)
Salary (numeric)
AI Impact / AI Exposure (categorical or numeric score)
Automation Risk (numeric score or category)
Experience (years or level)
Education (level)
Remote Ratio / Remote Work Share (numeric proportion)
Size
Data Facts:

Rows (job records): ~ [N]
Columns (features): ~ [M]
Time horizon: 2024 baseline vs 2030 projection
Key Limitations
Projection uncertainty: Growth rates to 2030 are forecasts; they depend on underlying assumptions and may not capture macroeconomic shocks.

Measurement of AI impact and automation risk: These are often modeled scores/categories; definitions may differ across sources.

Aggregation bias: Industry averages can hide within-industry variability across job families.

Missing data: Salary/experience/remote ratio may have missing or inconsistent coverage across industries.

Causality limitation: Observational data supports correlation and model-based explanation, not definitive causation.

Data Cleaning and ETL Methodology (Python Pipeline)
This section describes the reproducible pipeline from raw data → analysis-ready → Tableau-ready.

Overview of the ETL Flow
Step 1: Ingest
Load raw dataset (CSV/Excel) into pandas
Standardize column names (snake_case) and data types
Step 2: Cleaning
Handle missing values:

Remove rows with missing identifiers (e.g., Job Title, Industry)
Impute or drop missing numeric fields depending on impact (Salary, Growth, Risk)
Remove duplicates:

Exact duplicates or duplicates by key columns
Validate ranges:

Growth rate within reasonable bounds
Salary non-negative and within plausible limits
Remote ratio between 0 and 1
Risk score within its defined scale
Step 3: Feature Engineering
Created derived fields:

Risk Category: Low/Medium/High from automation risk thresholds
AI Impact Group: Low/Medium/High categorization
Experience Bands: Entry/Mid/Senior for segmentation
Standardized categorical values:

Normalize industry names (e.g., "IT", "Technology" → one label)
Ensure consistent job status labels
Step 4: Aggregation for KPIs and Summary Tables
Industry-level summaries:

Mean/median growth rate by industry
Mean salary by industry
Mean automation risk by industry
Share of declining/increasing roles per industry
Job-level summaries:

Top growing jobs (by growth rate)
Top declining jobs
Top paying jobs
Highest-risk jobs
Workforce summaries:

Education distribution
Experience distribution
Remote ratio by industry
Step 5: Output for Tableau
Export clean, analysis-ready table (row-level) for flexible filtering
Export aggregated tables (industry summary, job summary, risk segmentation, workforce summary)
Ensure Tableau-friendly types (numbers as numeric, categories as strings)
Quality Checks
Row count before vs after cleaning
Missing-value report per column
Summary statistics sanity check (min/median/max)
Category counts for Industry, Job Status, AI Impact, Risk Category
KPI and Metric Framework
This section defines our measurement system: what we track and how it's computed.

KPI Cards (Used Across Dashboards)
Core KPIs
KPI	Definition
Total Jobs	Number of job records in the dataset (or filtered subset)
Average Salary	Mean (or median) of salary across filtered jobs
Average Growth Rate	Mean projected growth rate across filtered jobs
Average Automation Risk	Mean automation risk score across filtered jobs
% Increasing	Count(status = increasing) / total
% Declining	Count(status = declining) / total
Analytical Metrics (For Deeper Charts)
Distribution Metrics
Salary distribution (histogram; optionally log-scale if long-tail)
Growth distribution (histogram)
Risk distribution (histogram)
Segment Metrics
Salary by AI impact group
Growth by AI impact group
Risk by job status
Salary by education level
Salary and growth by experience
Ranking Metrics
Top 10 growing jobs (highest growth rate)
Top 10 declining jobs (lowest growth rate)
Top 10 paying jobs (highest salary)
Top 10 risky jobs (highest risk)
Metric Definitions
Metric	Type	Definition	Why It Matters
Growth Rate	Numeric	Projected change in demand by 2030	Signals future hiring needs
Salary	Numeric	Compensation level per role	Indicates skill premium
Automation Risk	Numeric	Exposure of tasks to automation	Indicates vulnerability
AI Impact	Cat/Numeric	Degree of AI relevance or exposure	Explains growth/salary shifts
Remote Ratio	Numeric	Share of remote feasibility/work	Linked to pay and talent access
Education Level	Categorical	Highest education requirement	Hiring + curriculum planning
Experience	Numeric/Cat	Required years/level	A major salary driver
EDA with Visualizations and Written Insights
This section is organized to match our analytical themes and dashboard mapping.

7.1 Job Growth & Future Demand (EDA)
Visuals Included
Growth rate distribution (Histogram)
Industry vs average growth rate (Bar chart)
Top 10 growing jobs (Bar)
Top 10 declining jobs (Bar)
Job status distribution (Stacked bar)
AI impact vs growth (Scatter) and/or Growth by AI group (Boxplot)
Written Insights
Growth is not uniform across roles. The growth rate histogram shows a wide spread, with a small cluster of roles exhibiting very strong projected expansion while others are flat or negative. This indicates that demand is likely to concentrate in specific job families rather than rise evenly across the economy.

Industry differences are pronounced. The industry-level bar chart highlights sectors with consistently higher average growth rates. These industries represent priority areas for hiring investment and workforce expansion planning.

Declining roles are structurally different from growing roles. The "top declining jobs" list is dominated by roles that are routine, clerical, or repetitive in nature, whereas the "top growing jobs" list is more likely to include analytical, digital, AI-adjacent, or care-oriented work.

AI impact is positively associated with growth (descriptively). Scatter/boxplot views show that higher AI impact categories tend to have higher growth distributions. This supports the narrative that AI is not only automating tasks but also creating complementary roles.

7.2 Salary Analysis (EDA)
Visuals Included
Salary distribution (Histogram)
Salary by industry (Boxplot)
AI impact vs salary (Bar)
Experience vs salary (Scatter/Line)
Salary by education (Boxplot)
Remote vs salary (Scatter)
Written Insights
Salary distribution is typically right-skewed. The histogram suggests most roles cluster around a mid-range salary with a long tail of high-paying roles. This matters for decision-making because averages can be pulled upward by a few outliers; median salary is often a better "typical pay" metric.

Pay differs significantly across industries. Industry boxplots show clear separation: some industries have higher median salaries and wider salary variability, likely reflecting differences in value creation, productivity, and skill premiums.

AI impact roles show a salary premium (descriptively). The AI impact vs salary comparison indicates higher AI impact categories tend to command higher average salaries. This aligns with market behavior where scarce AI-related skills attract compensation premiums.

Experience raises salary, but not always linearly. Scatter/line plots typically show salary increasing with experience, with potentially sharper increases after mid-level experience and plateauing at senior levels.

Education is associated with higher salary bands. Salary-by-education boxplots often show higher median salaries for advanced degrees (Master's/PhD), suggesting education can be a differentiator for earnings potential.

Remote-enabled roles can correlate with higher pay. Remote vs salary patterns frequently show remote-friendly roles occupying higher salary ranges (especially in tech-oriented industries), though this can be influenced by role type and industry mix.

7.3 Automation Risk (EDA)
Visuals Included
Risk distribution (Histogram)
Top risk jobs (Bar)
Industry vs risk (Bar)
Risk vs job status (Boxplot)
Risk vs growth (Scatter)
Risk category distribution (Bar/Pie)
Written Insights
Automation risk varies across roles. The risk distribution typically shows a broad range, indicating not all jobs are equally exposed to automation.

High-risk roles cluster around routine tasks. The "top risk jobs" chart often features roles with standardized, repetitive workflows. This provides a concrete target list for reskilling programs.

Risk differs by industry. Industry risk bars/heatmaps show certain industries exhibit higher average exposure, suggesting sector-level workforce vulnerability.

Risk and job status relate meaningfully. Risk vs status boxplots frequently indicate declining roles have higher risk distributions, consistent with automation-driven displacement patterns.

7.4 Workforce Structure (Education, Experience, Remote)
Visuals Included
Education distribution
Experience distribution (Histogram)
Remote ratio by industry
Experience vs salary (Scatter)
Experience vs growth (Scatter)
Remote vs growth (Boxplot)
Written Insights
Education demand is uneven. Education distribution suggests the labor market demand is concentrated around a few education levels, providing signals for curriculum planning and candidate pipelines.

Experience is a strong differentiator. Experience distributions and its relationship with salary/growth highlight that workforce planning must account for seniority mix—not just headcount.

Remote work is industry-dependent. Remote ratio by industry demonstrates that remote feasibility is not universal; it is shaped by the nature of work in each sector.

Remote feasibility may influence outcomes. Remote vs salary and remote vs growth views help identify whether remote-enabled roles are associated with higher pay or stronger growth trajectories.

EDA Conclusion
Overall, EDA indicates that AI impact, automation risk, industry context, and human capital variables (education/experience/remote feasibility) jointly shape labor market outcomes. These descriptive patterns are validated using hypothesis testing, correlation analysis, and regression models in the statistical analysis section.

