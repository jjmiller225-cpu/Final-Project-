Food Safety Risk Signals: Montgomery County, Maryland

BUS 446 | Business Analytics Final Project

Team Members: Maxwell Blanc, Jace Miller, Ryan Winkler, and Mikey Vang
Project Date: November 2026
Analysis Tools: Microsoft Excel, Tableau, and Logistic Regression

Project Overview

Food safety inspections play an important role in protecting public health, but health departments must manage limited resources while overseeing thousands of establishments. This project examines food inspection records from Montgomery County, Maryland, to identify common violations, recognize patterns across different establishments, and evaluate whether historical inspection data can help predict future risks.

Rather than simply identifying which facilities experience the most violations, our analysis explores why certain inspection outcomes occur more frequently and how this information could support more effective inspection planning.

The study examines approximately 11,854 inspection records across 4,160 establishments, covering October 2022 through October 2024.

1. Data Collection and Preparation

Data Source: Montgomery County Food Inspection Dataset – Data.gov

The dataset contains information about establishment categories, inspection dates, inspection types, inspection results, and compliance with food safety requirements.

Microsoft Excel was used to prepare the inspection records for analysis. This involved organizing the observations, addressing inconsistencies, and developing variables needed for the visualizations and predictive model.

For analytical purposes, inspections with critical violations corrected or facility closures were classified as adverse outcomes.

Files: 01_Inspection_Data/

2. Tableau Visualizations and Findings

Tableau was used to examine inspection outcomes through visual comparisons, making it easier to recognize differences across establishments and identify recurring safety concerns.

Our visualizations focus on three areas:

Facility Risk: Comparing adverse inspection outcomes across restaurants, schools, carry-out facilities, and other establishments.

Common Violations: Identifying which food safety requirements are most frequently out of compliance.

Seasonal Patterns: Examining how violations, particularly refrigeration-related problems, change throughout the year.

Key Findings

Inspection Category

Finding

Public Middle Schools

40.5% adverse outcome rate

Restaurants

36.2% adverse outcome rate

Carry-Out Facilities

33.2% adverse outcome rate

Cold Holding Temperature

19.9% noncompliance rate

Rodents and Insects

15.5% noncompliance rate

One particularly interesting pattern involved cold holding temperatures. Violations increased during the summer months, suggesting that refrigeration performance and seasonal conditions deserve additional attention.

Files: 02_Tableau_Insights/

3. Logistic Regression and Predictive Analysis

After exploring the inspection data visually, we used logistic regression in Excel to investigate which factors were associated with higher risks of adverse inspection outcomes.

The analysis considered previous inspection performance, establishment category, and inspection type.

Predictive Findings

Risk Factor

Odds Ratio

Previous Adverse Inspection

2.41

Restaurant Category

1.77

Reinspection

0.30

Previous inspection performance emerged as an important predictor. Establishments with a prior adverse inspection had approximately 2.4 times the odds of experiencing another adverse outcome.

Although the model achieved approximately 70% overall classification accuracy, it also produced an 82.4% false-negative rate at the standard 0.50 cutoff.

This highlights an important limitation: a model may appear accurate overall while still overlooking many establishments that experience critical violations.

Files: 03_Risk_Prediction/

4. Business Case and Recommendations

The purpose of this project extends beyond identifying patterns. Our findings offer potential ways for Montgomery County health inspectors to allocate resources more effectively.

Based on the analysis, our team recommends:

Prioritizing Repeat Violators: Establishments with previous adverse inspection outcomes should receive closer monitoring and timely follow-up inspections.

Evaluating Predictive Thresholds: Reducing the model's classification cutoff from 0.50 to 0.30 could help identify more potentially unsafe establishments, although the change should be validated before implementation.

Strengthening Seasonal Prevention: Encouraging refrigeration maintenance before summer could help reduce cold holding temperature violations.

These recommendations demonstrate how business analytics can support decisions involving operational efficiency, resource allocation, and public safety.

Files: 04_Business_Case/

5. Project Documentation

This section contains the initial project overview and task plan that guided our team's research.

The documentation explains our research questions, dataset selection, proposed analytical methods, and overall project objectives.

Files: 05_Project_Context/

Project Takeaways

One of the biggest lessons from this project is that data becomes more valuable when it supports meaningful decisions.

Our analysis showed that food safety risks are not distributed equally across establishments. Certain facility categories experience higher adverse inspection rates, specific violations appear more frequently, and previous inspection performance provides useful information about potential future outcomes.

At the same time, our predictive model demonstrated why overall accuracy should not be the only measure of success. In public health applications, identifying potentially unsafe establishments can be more important than simply maximizing classification accuracy.

By combining Excel, Tableau, and logistic regression, this project demonstrates how historical inspection data can be transformed into practical insights for improving inspection priorities and supporting public health.

Data Limitations

This analysis focuses on inspection records from one county over approximately two years. Differences in inspection types, missing values, and repeated inspections may influence the results.

Additionally, the adverse-outcome classification was developed for this analysis and should not be interpreted as an official county pass/fail designation. The predictive model should be independently validated before being used for actual inspection decisions.

Source

Montgomery County, Maryland. Food Inspection Dataset. Data.gov.

https://catalog.data.gov/dataset/food-inspection

BUS 446 Final Project | Lenoir-Rhyne University | November 2026
