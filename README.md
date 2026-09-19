# TalentPulse Salary Prediction



An end-to-end ML regression pipeline predicting tech job salaries from a global job postings 

dataset — built as a capstone project applying skills from Excel, SQL, Python, Machine Learning, 

and data storytelling.



## Business Context



TalentPulse Analytics (a fictional HR-tech case study) uses a legacy lookup-table salary model 

with a $18,500 Mean Absolute Error (MAE) — far above the $8,000 industry benchmark. This project 

builds a data-driven regression pipeline to replace it, and evaluates whether it actually 

delivers on that promise.



## What This Project Covers



**EDA**: Uncovered and fixed a critical currency-mixing bug (salaries recorded in local 

&#x20; currencies without conversion) and a units bug in experience data (months mixed with years)

**Data Cleaning**: Handled 2,358 missing salary values, verified data integrity, encoded 

&#x20; categorical features appropriately (one-hot vs. ordinal, based on whether categories had 

&#x20; a natural order)

**Feature Engineering**: Built seniority flags, skill-based binary features, and tested/ 

&#x20; rejected a log-transform based on empirical evidence rather than assumption

**Modeling**: Compared Linear Regression, Random Forest, and Gradient Boosting; performed 

&#x20; hyperparameter tuning via GridSearchCV — and made an evidence-based decision to keep the 

&#x20; untuned model after tuning showed signs of overfitting on this dataset's size

**Evaluation**: Feature importance analysis and residual analysis by country and seniority, 

&#x20; surfacing findings that challenged the original business assumptions

**Business Memo**: A final benchmarking recommendation written for a non-technical HR audience



## Key Finding



Geography (specifically, being US-based) was the single dominant predictor of salary — far 

outweighing seniority, remote status, or specific technical skills. This directly challenged 

the case study's original framing, which emphasized seniority premiums and skill scarcity as 

primary drivers.



## Tools & Libraries



Python · Pandas · NumPy · Scikit-learn · Matplotlib · Seaborn · Jupyter Notebook



## Result



Best model (untuned Gradient Boosting): MAE = $28,014, R² = 0.45 — below the industry 

benchmark, with root causes (missing data, weak feature separation) identified and documented 

in the notebook rather than papered over.

