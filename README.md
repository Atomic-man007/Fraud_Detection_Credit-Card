# Fraud_Detection_Credit-Card
Credit Card Fraud Detection using python and scikit-learn

## Download dataset from kaggle
[Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

## Understanding and Defining Fraud

Credit card fraud is when someone obtains financial gain by using dishonest methods to get information from a cardholder without proper authorization. Skimming is the most common method, which duplicates information from the card's magnetic strip. Other methods include:
-manipulating genuine cards
-creating counterfeit cards
-using stolen/lost cards
-fraudulent telemarketing.

## Data Dictionary

The credit card fraud dataset contains transactions made by European cardholders over two days in September 2013. Out of 284,807 transactions, 492 were fraudulent, and the dataset is highly unbalanced. Principal Component Analysis (PCA) was used to maintain confidentiality, and all features except 'time' and 'amount' are principal components obtained using PCA. 'Time' is the seconds between the first transaction and subsequent transactions, and 'amount' is the transaction amount. The 'class' feature represents fraud (1) or non-fraud (0).


## Project Pipeline

The project pipeline can be briefly summarized in the following four steps:

- **Data Understanding:** Here, we need to load the data and understand the features present in it. This would help us choose the features that we will need for your final model.
- **Exploratory data analytics (EDA):** Normally, in this step, we need to perform univariate and bivariate analyses of the data, followed by feature transformations, if necessary. For the current data set, because Gaussian variables are used, we do not need to perform Z-scaling. However, you can check if there is any skewness in the data and try to mitigate it, as it might cause problems during the model-building phase.
- **Train/Test Split:** Now we are familiar with the train/test split, which we can perform in order to check the performance of our models with unseen data. Here, for validation, we can use the k-fold cross-validation method. We need to choose an appropriate k value so that the minority class is correctly represented in the test folds.
- **Model-Building/Hyperparameter Tuning:** This is the final step at which we can try different models and fine-tune their hyperparameters until we get the desired level of performance on the given dataset. We should try and see if we get a better model by the various sampling techniques.
- **Model Evaluation:** We need to evaluate the models using appropriate evaluation metrics. Note that since the data is imbalanced it is is more important to identify which are fraudulent transactions accurately than the non-fraudulent. We need to choose an appropriate evaluation metric which reflects this business goal.