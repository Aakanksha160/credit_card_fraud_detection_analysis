# Credit_Card_Fraud_Detection_Analysis
This Project divides into two section using two different datasets. First one is to build a robust fraud detection system and second one is to address all the insights and patterns of behaviors of credit card usage by creating dashboards.

1. Data Analysis
2. Machine Learning for Fraud Detection

# Data Analysis
In this Data Analysis project section, I explored Kaggle datasets related to credit card.In this dataset we have two different files one is for credit card and another one is for customer like customer age, sexual orientation, marital status, their jobs, education level etc.

We are showing all the data insights and graphs of all the transactions and customer details for 1 year.

All the data can be sorted and viewed through weekly for better convenience.

There are 2 different insights reports for transaction and customer analysis respectively.

# Insights

1. Overall revenue is 55M.
2. Total interest is 8M.
3. Total transaction amount is 46M.
4. Male customers are contributing 31M in revenue, while female customers are pulling in 26M.
5. In Low Income Groups, the usage of credit cards by male customers is very low, but in high income groups , the usage of credit cards by male customers is significantly higher.
6. Blue & Silver credit card together are contributing to 93% of all transactions.
7. Between all the states TX, NY & CA is contributing to 68%
8. Card Activation rate is 57.47%
9. The Delinquent rate is 6.07%

# Machine learning section

This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation.

Due to confidentiality issues, there are not provided the original features and more background information about the data.

- Features V1, V2, ... V28 are the principal components obtained with PCA
- The only features which have not been transformed with PCA are Time and Amount. Feature Time contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature Amount is the transaction Amount, this feature can be used for example-dependant cost-senstive learning.
- Feature Class is the response variable and it takes value 1 in case of fraud and 0 otherwise.

I investigated the data, checking for data unbalancing, visualizing the features and understanding the relationship between different features. I then investigated two predictive models. The data was split in 3 parts, a train set, a validation set and a test set. For the first three models, we only used the train and test set.

I started with RandomForrestClassifier, for which I obtained an AUC scode of 0.85 when predicting the target for the test set.

I followed with an AdaBoostClassifier model, with lower AUC score (0.83) for prediction of the test set target values.

I then followed with an CatBoostClassifier, with the AUC score after training 500 iterations 0.86.

I experimented with a XGBoost model. In this case, I used the validation set for validation of the training model. The best validation score obtained was 0.984. Then we used the model with the best training step, to predict target value from the test data; the AUC score obtained was 0.974.

I presented the data to a LightGBM model. I used both train-validation split and cross-validation to evaluate the model effectiveness to predict 'Class' value, i.e. detecting if a transaction was fraudulent. With the first method I obtained values of AUC for the validation set around 0.974. For the test set, the score obtained was 0.946.

## Cloning this repository

To clone this repository, use the following command:

```bash
git clone https://github.com/Aakanksha160/credit_card_fraud_detection_analysis.git

