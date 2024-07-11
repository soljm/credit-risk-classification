# Credit Risk Classification

From Module 20: Supervised Learning from the Data Analytics Boot Camp by Monash University and EdX.

By implementing skills learnt throughout the module, an attempt at the challenge has been submitted here.

## Contents

- `Credit_Risk` folder
  - `Resources` folder
    - `lending_data.csv` data file
  - `credit_risk_classification.ipynb` file with main code

## An Overview of the Analysis

From the Module 20 Challenge page on BootCamp Spot:

> In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

The label that this model is based around is the `loan_status` column in the original dataset. Within this variable, there are `0`'s and `1`'s, representing healthy loans and high-risk loans respectively.

After importing the data into a **Pandas DataFrame**, the data was split into `labels` and `features`, with the labels being the `loan_status` column and the features being the **DataFrame** without the `loan_status` column. The dataset was then split into training and testing datasets using the `train_test_split` function.

`LogisticRegression` was used to create a logistic regression model and fitted using the training data (`y_train` and `X_train`). A prediction using the testing data (`X_test`) was fitted to the logistic regression model and a confusion matrix was generated using this prediction and `y_test`.

A classification report was printed to assess how well the model does in predicting and classifying the different loans (`0`'s or `1`'s).

## Results

- 

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

- Machine Learning Model 1:
  - Description of Model 1 Accuracy, Precision, and Recall scores.

## Summary

Summarise the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

- Which one seems to perform best? How do you know it performs best?
- Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
