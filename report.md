
## Overview of the Analysis

The purpose of this analysis was to develop machine learning models to predict loan statuses in a financial dataset. The dataset contained information on various financial attributes, and the goal was to predict whether a loan would be classified as a healthy loan (0) or a high-risk loan (1).

The dataset was imbalanced, with a significantly larger number of healthy loans compared to high-risk loans. This imbalance posed a challenge for model performance, as the models could potentially have a bias towards predicting the majority class.

The analysis involved multiple stages of the machine learning process, including data preprocessing, feature engineering, model selection, and evaluation. Two machine learning models were used for comparison: Logistic Regression and Logistic Regression with oversampled data.

The Logistic Regression model was trained on the original imbalanced data, while the Logistic Regression model with oversampled data was trained on the oversampled dataset to address the class imbalance issue.


## Results


* Machine Learning Model 1 LogisticRegression:

balanced_accuracy_score =  0.9520479254722232
precision 0=1.00, 1=0.85
recall 0=0.99, 1=0.91
 

* Machine Learning Model 2 RandomOverSampler:

balanced_accuracy_score = 0.9936781215845847
precision 0=1.00, 1=0.84
recall 0=0.99, 1=0.99

## Summary


Based on the analysis, the RandomOverSampler model outperforms the Logistic Regression model in predicting loan statuses. The RandomOverSampler model shows higher recall for high-risk loans (class 1) while maintaining a good overall performance. This model successfully identifies more potential loan defaulters based on their credit risk, which aligns with the objective of minimizing false negatives.

In this problem, correctly identifying high-risk loans is of greater concern than potentially overclassifying good loans. Therefore, prioritizing recall for the high-risk loans becomes crucial. The RandomOverSampler model addresses this concern by achieving a higher recall for high-risk loans, while still maintaining high precision for healthy loans (class 0).

Considering these factors, the RandomOverSampler model is recommended for predicting loan statuses. It provides a valuable tool for managing credit risk assessments by effectively detecting potential loan defaulters. However, continuous monitoring and evaluation of the model's performance in real-world scenarios, along with consideration of any additional domain-specific factors, are essential for effective loan decision-making.