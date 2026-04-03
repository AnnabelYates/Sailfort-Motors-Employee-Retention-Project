# Sailfort-Motors-Employee-Retention-Project

## Executive Summary: 

Using Python, I performed an exploratory data analysis on employee data to identify sub-populations of employees who are more likely to leave the company. I ran a Chi-Square test which revealed that employee department was not a contributing factor behind employees leaving the company. After establishing basic profiles of employees less likely to be retained by the company, I created a logistic regression model, a random forest machine learning model, and an XGBoost machine learning model. Ultimately, I selected the random forest machine learning model to present to the company, which they would be able to use to predict whether employees would be retained by or leave the company. I also suggested the following recommendations to increase employee retention:

    1) Company-wide interventions, rather than department specific
    2) Policy of maximum of 5 projects 
    3) Ensure sufficient benefits, including confidential mental health care
    4) Research ways to handle employee burnout   

## Business Problem: 

Sailfort Motors seeks to reduce the rate of employees leaving the company. The HR team needs a model that is capable of accurately
predicting whether an employee will stay with the company or leave, so they can identify factors contributing to employees leaving. They will
use this information to implement interventions to improve employee retention. This will lead to cost and time savings as the company invests
heavily in training new employees.

### What employee sub-populations are most likely to leave the company, and can an accurate model be created to predict whether an employee will be retained by or leave the company?  

## Methodology: 

1) Exploratory data analysis using Python including data cleaning, feature engineering, removing duplicates, and addressing outliers.
2) Data visualizations using Seaborn and Matplotlib in Python to examine distributions of variables and relationships between variables.
3) Chi-Square test to investigate the impact employee department has on employee retention.
4) Logistic Regression model including creating a correlation heatmap and checking model assumptions
5) Tree-based machine learning models: random forest model and XGBoost model
6) Confusion Matrices and validation scores using validation data to select a champion model
7) Final confusion matrix, validation scores, and graph of feature importances using test data to predict future performance of the chosen model
8) Executive summary to communicate major findings and results

## Skills: 

Python: data modeling, machine learning, statistics, Chi-Square test, data visualization, exploratory data analysis (EDA), data cleaning, Logistic Regression Model, Random Forest Model, XGBoost Model, Seaborn, Matplotlib, Sklearn, Numpy, Pandas
Communication: executive summary

## Results and Business Recommendations: 

## Next Steps:
- Survey employees who have been with the company for greater than 7 years to identify factors that contributed to their loyalty. 
