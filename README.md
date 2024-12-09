# TELECOM CHURN PREDICTION
## BUSINESS UNDERSTANDING
### Project Overview
Customer churn is a critical challenge for telecommunications companies, including SyriaTel. Churn occurs when customers stop using the company's services, leading to revenue loss and increased acquisition costs to replace those customers. Retaining existing customers is far more cost-effective than acquiring new ones, making churn prediction vital for business sustainability.
#### Challenges:
•	**Identifying patterns of churn behavior:** Customer decisions can be influenced by various factors such as service quality, pricing, or competitive offers.

•	**Data quality and complexity:** Handling large datasets with diverse customer attributes and ensuring accuracy.

•	**Actionable insights:** Converting predictions into strategies that effectively reduce churn.

#### Stakeholders:
•	**Business Executives:** Focused on financial impact and strategic planning.

•	**Customer Service Teams:** Need insights to engage and retain at-risk customers.

•	**Data Science Team:** Responsible for developing, validating, and deploying predictive models.
#### Proposed Solution (Analysis & Modelling):
We will use historical customer data to build and evaluate machine learning models. The process involves:
1.	Data preprocessing and exploratory analysis.
2.	Training and comparing multiple classifiers (e.g., logistic regression, Decision Trees).
3.	Selecting the best model based on performance metrics.
#### Projected Conclusion:
The project aims to identify key indicators of customer churn and provide a robust predictive model. This will enable SyriaTel to proactively address churn risks, potentially improving customer retention and increasing revenue.
### Problem Statement
How can SyriaTel predict and reduce customer churn using historical data to improve customer retention and minimize revenue loss?

### Objectives:
1.	Develop a machine learning model to predict customer churn.
2.	Identify key factors contributing to churn.
3.	Provide actionable insights for customer retention strategies.


### Metrics of Success:
•	**Accuracy Score:** Measures overall correctness of predictions.

•	**Precision Score:** Ensures focus on true churners among predicted churners.

•	**Additional Metrics:** ROC-AUC and F1-score for balanced evaluation.

### Business Metrics:
•	Reduced churn rate.

•	Increased Customer Lifetime Value (CLV).

•	Improved ROI on retention strategies.

These metrics ensure that the model accurately identifies churn cases while minimizing false positives, allowing for efficient targeting of retention efforts.

## DATA UNDERSTANDING
### Data Source:
The dataset is sourced from Kaggle through github [SyriaTel Customer Churn](https://www.kaggle.com/becksddf/churn-in-telecoms-dataset).
The data is based on a Syrian Telecom company called SyriaTel, containing customer attributes and churn status.
### Data Size:
•	**Rows:** 3,333
•	**Columns:** 21

### Columns:
•	**Churn:** Target variable (1 = churned, 0 = not churned).

#### Categorical Features:
•	state
•	area code
•	international plan
•	voicemail plan

#### Continuous Columns:
•	account length
•	number vmail messages
•	total day minutes
•	total day calls
•	total day charge
•	total eve minutes
•	total eve calls
•	total eve charge
•	total night minutes
•	total night calls
•	total night charge
•	total intl minutes
•	total intl charge
•	customer service calls

## DATA PREPARATION AND ANALYSIS
The data had already been cleaned from our source.
### Exploratory Data Analysis
- **Univariate:** both numerical and categorical.
  
- **Bivariate:** boxplots and stacked bar charts
  
- **Multivariate:** correlation heatmap
![image](https://github.com/user-attachments/assets/85b8a695-a5a3-421c-b6b7-916d2aac6bbc)

## MODELING
Three models:
### 1. Baseline Model: Logistic Regression
![image](https://github.com/user-attachments/assets/c577a27b-dc02-4ef5-95b7-462b0f29a5bd)
Logistic Regression Accuracy: 0.86

Logistic Regression Precision: 0.58

Logistic Regression Recall: 0.21

Logistic Regression F1-Score: 0.31
### 2. Second Model: Decision Tree Classifier

![image](https://github.com/user-attachments/assets/b1edfbda-11d9-4079-a1e2-59e41363e381)
Decision Tree Accuracy: 0.92

Decision Tree Precision: 0.74

Decision Tree Recall: 0.74

Decision Tree F1 Score: 0.74

### 3. Tuned Model: Hyperparameter-tuned Decision Tree 
![image](https://github.com/user-attachments/assets/0a7114ea-ff8e-4f8d-a6d8-ac1dee0aad3b)
Tuned Decision Tree Accuracy: 0.94

Tuned Decision Tree Precision: 0.88

Tuned Decision Tree Recall: 0.71

Tuned Decision Tree F1 Score: 0.79

The Tuned Decision Tree model performs best due to its high precision, AUC, and interpretability.

## CONCLUSION
1.	The Tuned Decision Tree is the most suitable model for this project, as it met and exceeded the success criteria (accuracy ≥ 85%, precision ≥ 80%). This model is robust and can effectively predict customer churn while minimizing false positives.
2.	The Basic Decision Tree performed well in accuracy but fell short on precision, showing that hyperparameter tuning plays a crucial role in improving model performance.
3.	The Logistic Regression model is unsuitable for deployment due to its significantly lower precision, meaning it might misclassify too many customers as churned, leading to inefficient allocation of retention efforts.
4.	Insights highlight high churn risks among customers with month-to-month contracts.

## RECOMMENDATIONS
1.	Develop targeted retention campaigns for high-risk segments (e.g., short-tenure customers).
2.	Offer incentives for customers to shift to longer contracts.
3.	Monitor churn risk factors continuously and update models with new data.

 ## NEXT STEPS
 #### 1. Deployment Monitoring
 #### 2. Improve the model with Random Forest
 #### 3. Collecting more data.

### Limitations
The analysis has limitations, including the reliance on historical data and the potential for biases in the dataset.










