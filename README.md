# Credit_Risk_Analysis
## Overview
The purpose of this exercise is to build different machine learning models that can help determine credit risk. Once complete, the models were evaluated to determine if any were suitable options to use or to use as a starting place to grow from.
## Machine Learning Models
In this analysis, we will evaluate the balanced accuracy score, precision, and recall scores for the following models:
### RandomOverSampler
Precision and recall are high for the majority class, but the precision is low for the minority class. Meaning that of 100 people who were classified as high risk, only one was truly high risk, and 99 were falsely identified. The f1 score is also low and is explained by the profound imbalance between the precision and recall for high risk. The balanced accuracy score is 65%.
<img width="831" alt="Screen Shot 2022-04-17 at 6 39 33 PM" src="https://user-images.githubusercontent.com/92702922/163736339-d5422e9a-9287-451c-835c-09a757189418.png">
### SMOTE
The precision and recall results are the same as the RandomOverSampler model, but the accuracy decreased to 63% in this model. The recall slightly decreased for the high risk group, and the F1 score stayed the same. The balanced accuracy score is 63%.
<img width="840" alt="Screen Shot 2022-04-17 at 6 40 43 PM" src="https://user-images.githubusercontent.com/92702922/163736370-ab95a307-2892-4c40-886a-126455bef790.png">
### Cluster Centroids
The precision for the high risk group stayed the same as previous models, but the recall for the low risk group decreased significantly which caused a decrease in its f1 score as well. The balanced accuracy score is 44%.
<img width="830" alt="Screen Shot 2022-04-17 at 6 43 49 PM" src="https://user-images.githubusercontent.com/92702922/163736461-38fc3259-fc90-4472-95da-a1ea349908f9.png">
### SMOTEENN
There was a significant increase in the recall for both groups which improved the f1 score for the low risk group. There is such a big imbalance between the precision and recall of the high risk group, which is why we aren't seeing an improvement in the f1 score even with the improvement in the recall score. The balanced accuracy score is 54%.
<img width="832" alt="Screen Shot 2022-04-17 at 6 45 25 PM" src="https://user-images.githubusercontent.com/92702922/163736502-86e81a34-9e9c-47d6-bfc5-f2f535a95d09.png">
### BalancedRandomForestClassifier
The precision finally increased for the high risk group, which also increased the f1 score. The recall increased for both groups, putting the recall for the low risk group at 0.91 and a resulting f1 score of 0.95. The balanced accuracy score is 79%.
<img width="817" alt="Screen Shot 2022-04-17 at 6 52 04 PM" src="https://user-images.githubusercontent.com/92702922/163736744-72aab706-28ee-4fd7-a39a-ebe3dd2c6a78.png">
### EasyEnsembleClassifier
The precision and recall scores for the high risk group significantly increased, putting the recall score at 0.91. The recall score increased in the low risk group bringing it to 0.94. The balanced accuracy score is 94%.
<img width="820" alt="Screen Shot 2022-04-17 at 6 54 16 PM" src="https://user-images.githubusercontent.com/92702922/163736834-857c9860-8172-409a-802a-d2d010404cbe.png">
## Summary
In conclusion, although there is a gradual increase in effectiveness from model to model, even the best model, EasyEnsembleClassifier, does a poor job at misclassifying credit risk as positive for the high risk group. Therefore, I would not recommend any of these models for use until further improvements are made to reduce bias in the high risk group classifications.
