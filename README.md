# Predictive-Customer-Model-Python
Task: please recommend which of these 1000 new customers should be targeted to drive the most value for the organisation.
Solution: 
1. Use python to clean data, including addressing missing values and outliers and formatting data types.
2. Conduct RFM (recency, frequency, monetary value) analysis to calculate RFM scores as a target variable based on the training data set(existing customers' data set). If RMF_score >=3.5, the customer is a potential buyer and we should allocate more resources, and vice versa.
3. Plot the distribution of the target variable to judge whether it's balanced or imbalanced. Here the distribution is imbalanced, so we use SMOTE (Synthetic Minority Oversampling Technique) method to increase the number of minority classes for the later model building. To verify whether it's worth balancing the target variable. Here we build two sets of machine learning models, one uses the original and imbalanced data set and the other uses the SMOTE balanced data set. 
4. Plot the distributions of feature variables to get insights and judge whether it's normal or skewed.
5. In order to predict which of the 1000 new customers should be targeted, we build 8 models, including a logistic regression model, decision tree, SVC, K Nearest Neighbor, Random forest, Adaboost, Stochastic Gradient Boosting, Xgboost, based on the oversampled data set. Compared with accuracy score and F1 score, the random forest performs the best in both Non-SMOTE models and SMOTE models. But in Non-SMOTE models, although the accuracy scores and F1 score are quite high, the potential customers F1 score is 0, which means the prediction for the target customers is inaccurate. In SMOTE models, the potential customers F1 score is almost the same as the total F1 score. Therefore, it's significantly important to use SMOTE method to balance the target variable.
6. With the best random forest model with accuracy score around 72.88% and F1 score around 0.6677, the 1000 new customers data is cleaned and input. Around 22.24% of the 1000 new customers should be targeted to drive the most value for the organisation. The targeted name list is also output as a result.
