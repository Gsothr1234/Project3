SYRIATEL CUSTOMER CHURN
PHASE 3 PROJECT
STUDENT NAME: SADI KIRI

BUSINESS UNDERSTANDING
Overview
In the telecommunication industry customer churn is typically used to refer to the rate at which a company is bleeding customers as they discontinue the services, they employ with their particular service provider. This is an undesirable result as it results in revenue loss and can indicate the performance of the service provider brand image in the public eye. Furthermore, this requires further investment of resources on the service provider part as revenue is diverted to acquire new customers as it is typically more expensive to attract new customers than to retain existing ones. Given this SyriaTel a telco company facing a significant amount of churn wishes to be able to predict factors that cause customers to be more likely to churn in order to solidify its market share and identify the key features that can be improved to reduce churn.
Problem Statement
Given the substantial dangers churn poses our stakeholders in the product improvement department in SyriaTel has provided data to aid in identifying key features that influence churn. The goal is to develop a predictive model that can identify key customer factors that indicate churn and subsequently target these key areas that can reduce churn in order to position itself as a market leader.

Data Exploration
The dataset employed in this analysis originates from Kaggle and pertains to SyriaTel. The predictive models utilized for the analysis include logistic regression, decision tree, and random forest.
The figure below shows correlation heatmap between target variable and key features analyzed
 

The figure above shows churn data in our dataset with an average of about 15%

Modelling
1.)	Logistic regression (Benchmark):
precision    recall  f1-score   support

       False       0.95      0.77      0.85       709
        True       0.38      0.78      0.51       125

    accuracy                           0.77       834
   macro avg       0.66      0.78      0.68       834
weighted avg       0.87      0.77      0.80       834
The model is performing relatively well with an overall accuracy of 77% it is effective in identifying non churn cases with an f1 score of 85 but less effective for the churn cases with an fl score of 51
2.)	Decision Tree:
precision    recall  f1-score   support

       False       0.94      0.90      0.92       709
        True       0.54      0.68      0.60       125

    accuracy                           0.87       834
   macro avg       0.74      0.79      0.76       834
weighted avg       0.88      0.87      0.87       834

The model shows an improved accuracy over the logistic regression with an accuracy of 87% and a slight improvement in precision when predicting accurate cases of churn at 60

3.)	Random Forest 

        precision    recall  f1-score   support

       False       0.97      0.98      0.97       709
        True       0.86      0.81      0.83       125

    accuracy                           0.95       834
   macro avg       0.91      0.89      0.90       834
weighted avg       0.95      0.95      0.95       834



This represents the best model so far with a high f1 score for both churn and non churn and an overall accuracy of 95%

Hyper-Parameter Tuning:

              precision    recall  f1-score   support

       False       0.96      0.98      0.97       709
        True       0.86      0.79      0.82       125

    accuracy                           0.95       834
   macro avg       0.91      0.88      0.90       834
weighted avg       0.95      0.95      0.95       834

The hyperparameter tuned RandomForest model has an f1 score of 97% with an f1 score of 82% for churn cases.


When evaluating the performance of our hyperparameter tuned model the accuracy improved to 97% with an f1 score of 82% for churned cases.

Conclusion 

•	The random forest model was the best performing model, showing an accuracy of 95% with an fl score of 97% for non churn cases and 82% for churn cases indicating a robust model. Features of note in this model are shown below; of note are total day minutes, customer service calls total day minutes and international plan being the most significant while number vmail messages, account length and total eve calls are the least


 
 

•	Frequent customer calls indicate a significant higher chance to churn

•	Users who are on the international plan are also more likely to churn
•	Users who use more total day minute are more likely to churn an indicator of either high charge are connectivity issues during high volume periods 
Recommendations

•	Customer service appears to be a key issue further investigation and analysis into what common problems customers experience can help for a targeted fix that will alleviate the issue.

•	Investigate pricing structure as daily minutes has seen to be a significant factor in churn could indicate high prices as opposed to competitor market survey against competitors is recommended

•	Review international plan cost could be a key driver in this challenge may need to restructure plan to entice customers to stay

Next Steps
•	A breakdown into customer service calls to target key issues using key word searches
•	Investigate connectivity issues by area
•	Investigate if technology can handle high volumes during the day time as that could also cause the drop offs



