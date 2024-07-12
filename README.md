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

For this machine learning model:

- Accuracy score: 0.99 (99%)
- Healthy loan (`0`): Support - 18765

  - Precision: 1.00 (100%)
  - Recall: 0.99 (99%)

- High-risk loan (`1`): Support - 619

  - Precision: 0.84 (84%)
  - Recall: 0.94 (94%)

- Macro average (when classes are imbalanced):

  - Precision: 0.92 (92%)
  - Recall: 0.97 (97%)

## Summary

Looking at the macro averages, the model performs quite well as the scores are all above 0.90 (90%). However, as the precision score of class `0` is exactly **1.00**, it does raise suspicion as to whether the model actually works properly, as this implies that there were no false positives (loans that were identified as healthy even though it was high-risk).

On the other hand, looking at just the `1`'s, the scores are relatively low compared to the `0` scores, meaning the detection of high-risk loans is lower than the detection of healthy loans. 

Concluding, this model is not recommended to be used to determine the creditworthiness of borrowers at its current state until more testing is done or accuracy of the model can be verified.
