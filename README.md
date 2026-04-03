# Sailfort-Motors-Employee-Retention-Project

## Executive Summary: 

Using Python, I performed an exploratory data analysis on employee data to identify sub-populations of employees who are more likely to leave the company. I ran a Chi-Square test which revealed that employee department was not a contributing factor behind employees leaving the company. After establishing basic profiles of employees less likely to be retained by the company, I created a logistic regression model, a random forest machine learning model, and an XGBoost machine learning model. Ultimately, I selected the random forest machine learning model to present to the company, which they would be able to use to predict whether employees would be retained by or leave the company. I also suggested the following recommendations to increase employee retention:

1) Company-wide interventions, rather than department specific
2) Policy of 5 current projects maximum
3) Ensure sufficient benefits, including confidential mental health care
4) Research ways to address employee burnout   

## Business Problem: 

Sailfort Motors seeks to reduce the rate of employees leaving the company. The HR team needs a model that is capable of accurately
predicting whether an employee will stay with the company or leave, so they can identify factors contributing to employees leaving. They will
use this information to implement interventions to improve employee retention. This will lead to cost and time savings as the company invests
heavily in training new employees.

#### What employee sub-populations are most likely to leave the company, and can an accurate model be created to predict whether an employee will be retained by or leave the company?  

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

Performing an exploratory data analysis revealed employee sub-populations at risk for leaving Sailfort Motors.

#### Employees most at risk of leaving the company: 

- Feel unsatisfied, overworked, and under-appreciated
due to heavy work loads and no recent promotions.
- Feel satisfied and perform well at their work, but work
very long hours.
- Have 6 or more projects.
- Have only 2 projects.
- Feel unsatisfied and perform poorly at their jobs. 

Most employees who left the company worked extremely high hours every month. Even though they worked the longest hours out of all employees, these employees were less likely than their peers who worked shorter hours to receive promotions within the last 5 years. 

<img width="945" height="225" alt="image" src="https://github.com/user-attachments/assets/c3896dfe-f3b2-460a-aa1e-7374acc8ebd4" /> 

Visualizing which employees left by how many projects they currently had revealed startling differences of employee retention rates. All employees who had 7 projects left the company, and about half of those with 6 projects left the company. Interestingly, having too few projects also had a negative impact on employee retention. Over half of all employees with only 2 projects left the company. Evidence indicates having 3 to 5 projects is an ideal workload for most employees.   

<img width="395" height="275" alt="image" src="https://github.com/user-attachments/assets/ea7831d8-a288-443e-a812-dc9223c32180" /> 

A Chi-Square test determined that employee department had little or no impact on the rate employees left the company. No employee in one department is statistically more likely to leave than any other department. Due to this and a heightened risk of overfitting, this variable was not used in model development. To ensure the model is able to be used in the future without subjective employee input, satisfaction score was dropped also. 

### Summary of model results:
The scoring metric I was most interested in is recall, as this would find as many potential employees leaving the company as possible. I wanted to reduce false negatives (identifying people as staying when they will actually leave). This is generally used in employee turnover models because it is generally more expensive to lose a trained employee than initiate some form of intervention. The model that performed best was the random forest machine learning model. This model performed successfully across all metrics. The model performed identically on the test data as the validation data for recall, which was 0.927. This means that the model correctly identified 92.7% of all people who leave the company. The F1 and precision scores increased for the model with the test data, but are within an expected variation. The accuracy score was 0.968, the precision score was 0.889, and the F1 score was 0.907. Additional testing using novel test data revealed
the model is excellent at correctly identifying both employees who will leave the company and those who will be retained by the company. Since the model performed as well on the unseen test data as the validation data, which indicates the model is not overfitted to the training data, I am confident the company will be able to use this model on new data with successful results. 

The confusion matrix showed the success of the model's performance. Only 29 employees who left were missed by the model after predicting about 10,000 employees.  In the future, the model is expected to correctly predict 96.9% of employees who will be retained and 92.7% of employees who will leave. 
 
<img width="346" height="262" alt="image" src="https://github.com/user-attachments/assets/611a00ed-79da-4934-ac92-000f79c658c1" />

The most important features for the model were projects, total hours worked for the company over an employee's entire employment there, and latest performance scores. Hours per month also contributed significantly. Tenure, being under appreciated, and salary level had a limited influence on the model. Being a hard worker, high performer, having a work accident, being overworked, having a recent promotion and being full time had no impact on the model.

<img width="378" height="350" alt="image" src="https://github.com/user-attachments/assets/6d735486-42be-447d-8a4f-91b716052b03" />

### Recommendations for Sailfort Motors:

- Evidence suggests that there is not a major issue among specific departments affecting employee retention rate. Interventions can be implemented more broadly among the employee population rather than tailoring the approach to select departments.
- Implement a policy to cap the amount of projects employees can work on at one time to 5. Between 3 and 5 projects at a time would be ideal for most employees.
- Data indicates employee burnout is pervasive throughout the company due to a culture of long hours and heavy workloads. Ensure benefit packages are sufficient and investigate whether employees have confidential access and awareness of mental health care, such as online therapy.
- Employee burnout is a common issue in issue in corporate workplaces. Research ways other companies have successfully addressed this issue. 

## Next Steps:
- Survey employees who have been with the company for greater than 7 years to identify factors that contributed to their loyalty.
- Investigate factors behind extremely long monthly hours of some employees. This could reveal ways to boost productivity for employees while reducing long monthly hours which is related to decreased employee retention rates. 
