# Comparing Classifiers

## Problem Statement

The business problem is to predict whether a client will subscribe to a term deposit based on various socio-economic and campaign-related features. This prediction can help the bank optimize its marketing strategy by targeting clients who are more likely to subscribe, ultimately improving campaign effectiveness and reducing costs.

Please use the following notebook to go through the analysis: https://github.com/dashao/mlai/blob/main/classifiers/classifiers_comparison.ipynb

## Key Findings

We evaluated four machine learning models to predict term deposit subscriptions: K-Nearest Neighbors (KNN), Logistic Regression, Decision Tree, and Support Vector Machine (SVM).

1. The Support Vector Machine had the highest training time (253 seconds), significantly longer than other models. Logistic Regression had the shortest training time (~0.05 seconds), making it suitable for real-time training scenarios.

2. Logistic Regression showed a reasonable balance with a training accuracy of 89.9% and a testing accuracy of 89.9%. KNN also performed well, but the Decision Tree showed overfitting, with very high training accuracy (99.4%) and lower test accuracy (83.6%).

3. Logistic Regression achieved the highest precision (68.5%), meaning it minimized false positives more effectively compared to other models.

4. The Decision Tree had the highest recall (33.2%), which indicates it identified more true positives but also introduced more false positives.

5. K-Nearest Neighbors achieved the highest F1 score (32.6%), indicating the best balance between precision and recall among the models evaluated. However, there is still room for improvement, particularly given the class imbalance.

Overall, K-Nearest Neighbors appears to be the most suitable model for this business problem, providing the highest F1 score and good performance across other metrics. Logistic Regression also performed well with the highest precision and a reasonable balance between training time and accuracy, making it another strong candidate depending on business priorities.



## Next Steps and Recommendations

1. Consider further improving the models by using additional techniques to handle class imbalance, such as oversampling the minority class.

2. Grouping clients by common behaviors might reveal hidden patterns that could improve model accuracy and recall.

3. Deploy the selected model and set up a monitoring system to track its performance over time. The model should be retrained periodically as new data becomes available to ensure it adapts to changing customer behaviors.

4. Integrate the model’s predictions into ongoing marketing campaigns.