# ML-Credit-Card-Default-Prediction---Classification
### Supervised Machine Learning 

## Business Objective
This project is aimed at predicting the case of customers' default payments in Taiwan. From the perspective of risk management, the result of predictive accuracy of the estimated probability of default will be more valuable than the binary result of classification - credible or not credible clients.

## Dataset Overview
- Dataset contains 30,000 rows and 25 columns.
- There no duplicate values.
- There are no null values.
- Some of the columns are LIMIT_BAL, SEX, MARRIAGE, EDUCATION, AGE, etc.

## Data PreProcessing
- For better readability, some of the column names have been changed.
- Based on variables description, substituted the actual value in place of numbers. Example - For the column EDUCATION, 1 is replaced with Graduate School, 2 is replaced with University. For the column SEX, 1 is replaced with Male. Same is applied on Marital Status.
- Column ID has been dropped.

## Exploratory Data Analysis
- From the dataset give, we observe that there is a data imbalance. There are only 6636 records for default.
- Female have more number of credit cards than men. Around 21% of total female clients default from payment while 24% of total male clients default from payment.
- Most (i.e. around 82%) of the credit card clients have went to a University or a Graduate School. Most (i.e. around 82%) of the credit card clients have went to a University or a Graduate School.
- Around 19% of credit card clients who went to a Graduate School will default on their payments while 25% of credit card clients who went to a High School will default on their payments.
- Credit card clients who are single, are more in number than Credit Card clients who are married. Around 21% sinlge credit card clients default on their payment while 23% married credit card clients default on thier payment.

## Feature Engineering
- Used Yeo-John Transformation for transformation instead of Box-Cox Transformation as their were negative values in some of the columns.
- Used StandardScaler for feature scaling.
- Used Synthetic Minority Oversampling Technique(SMOTE) to balance our dataset.
- Used OneHotEncoding for encoding of categorical features.

## ML Model Implementation
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- XGBoost

## Evaluation Metric Selection
For our current problem, we would be mainly looking at the Recall/Sensitivity score of all the models and based on that we would choose our model. The reason being - It is important in credit card default cases where it doesn’t matter whether we raise a false alarm but the actual positive cases should not go undetected!

## Summary
- XGBoost gives a very good recall value which is essential to our project.
- This project was successfully deployed thus enabling the bank to reach out to non-defaulting potential customers.
