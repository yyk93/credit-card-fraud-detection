##### Author: Vincent Yeo

# Credit Card Fraud Detection

#### Background:
As a credit card company, it is important to offer consumer protection against fradulent transaction so that consumers don't pay for purchases that they did not make.


#### Dataset
CreditCardFraud Dataset by Machine Learning Group - ULB at [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud#creditcard.csv)

#### Task:

Classify which transaction is fradulent.

#### Results and Analysis

|Model|Test AUC|Precision|Recall| F1-Score|
|-----|--------|---------|------|--------|
| Xgboost| 0.945 | 4.00% | 92.85% | 7.68% |
| Logistic Regression| 0.951 | 4.21% | 93.87% | 8.07% |
| Decision Tree Classifier | 0.929 | 2.27% | 92.85% | 4.43% |

Logistic Regression has the overall best performance of Test AUC of 0.951 using undersampled data

##### Intepretation of the Best Classifier
Based on precision, each prediction of either "Fraudulent", or "Not Fraudulent" would be realised truely about 4.21% of the time.

Based on recall, each prediction of "Fraudulent" has about 93.87% being correct.

Based on f1 score of the "Fraudulent", the weighted average of the precision and recall is 8.07%

| |Pred: Fraudulent  | Pred: Not Fraudulent|
|-------|-------|-------|
|True: Fraudulent  |  92  | 6|
|True: Not Fraudulent |2090  |54774|

#### Limitations and Future Works

+ Given the limited computation power, only undersampled dataset is used in training


+ Tried Kfold split to get the mean AUC score for train and test and other metrics but not much significant improvement (see table below)

|test|train_auc|test_auc|precision|recall|f1|
|------|------|------|------|------|------|
|0|0.971433|0.971433|0.041207|0.912878|0.078276|
|1|0.969486|0.969486|0.054688|0.905485|0.097396|
|2|0.941402|0.941402|0.020136|0.876693|0.039176|



