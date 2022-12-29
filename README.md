# Credit_Risk_Analysis
  System: Jupter Notebook, Python, Scikit-learn, SMOTEENN
  
# Overview
In 2019, over 19 million Americans had at least one unsecured personal loan. FinTech firms analyze a large amount of data to predict trends and optimize lend. Using Python, we needed to build and evaluate several machine-learning models to predict credit risk. Being able to predict credit risk with machine learning algorithms can help banks and financial institutions predict anomalies, reduce risk cases, monitor portfolios, and provide recommendations on what to do in cases of fraud. Fast Lending, a peer-to-peer lending service wants to use machine learning to predict credit risk. We need to help Jill, the Lead Data Scientist, with using machine learning to lead to more accurate identification of good candidates for a loan to lower default rates.

# Results
  - Using Python and Scikit-learn to predict credit risk
  - Compare the strengths and weaknesses of machine learning models
  - Assess how well a model classifies and predicts data
  - Using resampling and boosting 

### Naive Random Oversampling
![Naive Randome Oversampling](https://user-images.githubusercontent.com/108844775/209919724-0015c1c9-b88b-485c-bfdb-d5b3fa4e103d.png)
  - Balanced Accuracy Score: .6438627638488825
  - Precision: Low for High Risk loans, High for Low Risk loans
  - Recall: 59% Low-Risk loans 
  - F1: .74 -> We want F1 to close to 1 but it's not meaning that the model did a poor job in predicting whether loans were high or low risk.
 
### SMOTE Oversampling
![SMOTE Oversampling](https://user-images.githubusercontent.com/108844775/209919789-dad47f9e-bcaa-4b08-9834-b65b44c1f7d3.png)
  - Balanced Accuracy Score: .6628910844779521
  - Precision: Low for High-Risk loans, High for Low-Risk loans
  - Recall:69% Low-Risk loans
  - F1: .82 -> We want F1 to close to 1, it did better than Naive random oversampling but still not close enough to 1.

### Undersampling
![Undersampling](https://user-images.githubusercontent.com/108844775/209919806-2d60952f-c831-4845-9170-4a83c04e5a3b.png)
  - Balanced Accuracy Score: .6628910844779521
  - Precision: Low for High-Risk loans, High for Low-risk loans
  - Recall: 40% Low-Risk loans
  - F1: .57 -> Worst model 

### Combination of Under and Oversampling
![Combination of Under and OverSampling](https://user-images.githubusercontent.com/108844775/209919708-9749ff81-258a-459a-bfe2-90ecb72132dd.png)
  - Balanced Accuracy Score: .5447339051023905
  - Precision: Low for High-Risk loans, High for Low-risk loans
  - Recall: 57% Low-Risk loans
  - F1: .72 

### Balanced Random Forest Classifier
![Balanced Random Forest Classifier](https://user-images.githubusercontent.com/108844775/209919646-084b30bd-2c63-4717-9d52-6d933b1c793e.png)
  - Balanced Accuracy Score:.7885466545953005
  - Precision: Low for High-Risk loans, High for Low-risk loans
  - Recall: 87% Low-Risk loans
  - F1: .93 -> Close to 1.  

### Easy Ensemble AdaBoost Classifier
![Easy Ensemble AdaBoost Classifier](https://user-images.githubusercontent.com/108844775/209919716-35ba4318-555e-4636-b1b1-823b462c60d9.png)
  - Balanced Accuracy Score: .9316600714093861
  - Precision: Low for High-Risk loans, High for Low-risk loans
  - Recall: 94% Low-Risk loans
  - F1: .97 -> Closest to 1. Best model
 
# Summary
In conclusion, using the Easy Ensemble AdaBoost Classifier is the best model. The balanced accuracy score in binary and multiclass classification problems to deal with imbalanced the best value is 1 and the worst is 0. As you can see the Easy Ensemble AdaBoost Classifier is at 0.93 which tells us that the logistic regression model did a good job of predicting whether or not loans are at High-Risk or Low-Risk. As well as the recall score falling within the 0 and 1 range, with the number closest to 1 being the best model. By far using the Easy Ensemble AdaBoost Classifier model would help identification of good candidates for loans to lower default rates. The other models would give more fraudulent loans.

