# Lead Scoring Case Study

Logistic regression model that scores leads for X Education so the sales team can prioritize the most promising ("hot") leads.

## Problem

X Education sells online courses to professionals. It gets many leads from websites, search and email, but converts few. The goal is a lead score where a higher score means a higher chance of becoming a paying customer.

## Approach

1. Clean the data: replace "Select" placeholder values, drop columns dominated by a single value, treat missing values (about 69% of rows retained)
2. Create dummy variables, split train/test, scale features
3. Build the model iteratively (four models), removing features with high p-values or VIF
4. Evaluate with ROC curve and an accuracy/sensitivity/specificity sweep to choose the cutoff
5. Check the precision/recall trade-off as an alternative view
6. Predict on the test set

## Results

- ROC AUC: 0.86, as reported in the notebook's ROC analysis
- In the cutoff sweep, a 0.4 probability cutoff gives accuracy 0.79, sensitivity 0.81 and specificity 0.77

## Files

| File | Purpose |
| --- | --- |
| `Lead_Scoring_case_study _Anand .ipynb` | Analysis and model |
| `Lead_Scoring_Assignment.pdf` | Assignment brief |
| `Summary of Lead scoring case study .pdf` | Summary of findings |
| `Subjective Questions Answers.pdf` | Written answers |

## Stack

Python, pandas, scikit-learn, statsmodels, matplotlib, seaborn
