**Airline Passenger Satisfaction Analysis**

**Overview**
This repository contains an in-depth analysis of airline passenger satisfaction. The project focuses on extensive exploratory data analysis (EDA), handling missing data, and building predictive models. We explore various factors that impact passenger satisfaction and aim to identify patterns and insights.

**Key Findings**

Gender Distribution: Both male and female passengers show a higher number of dissatisfied customers compared to satisfied ones.

Customer Type: Loyal passengers constitute a significant portion. Among them, the ratio of satisfied to dissatisfied passengers is nearly 49:51.

Age Groups: Dissatisfaction is prevalent among passengers aged 7 to 38 and 61 to 79. Conversely, passengers aged 39 to 60 tend to be more satisfied.

Online Boarding and Departure/Arrival Time: Eco Plus class passengers experience high dissatisfaction when departure/arrival times are inconvenient (Departure/Arrival_time_convenient = 0), even with efficient online boarding.

Label Encoding: Categorical variables have been encoded for modeling purposes.

**Data and Models**

**EDA :** Extensive visualizations were used to explore the dataset.

**Missing Data Handling:** Strategies such as imputation or removal were applied.

**Outliers Detection and Removal** 

**Correlation among Features**

**Top 10 Feature Selection through Chi-Square :** ['Type_of_Travel', 'Class', 'Flight_Distance', 'Inflight_wifi_service',
       'Online_boarding', 'Seat_comfort', 'Inflight_entertainment',
       'On-board_service', 'Leg_room_service', 'Cleanliness']

**Feature Importance using Wrapper Method :** So only these six features are inherently important in contributing towards passenger satisfaction. However, we will again cross-check with another feature importance deciding method.
['Type_of_Travel', 'Class', 'Inflight_wifi_service', 'Online_boarding', 'Seat_comfort', 'Inflight_entertainment']

**Building Models :**

Logistic Regression (clf1): A linear model that estimates probabilities for binary classification.

Gaussian Naive Bayes (clf2): A probabilistic classifier based on Bayes’ theorem.

K-Nearest Neighbors (clf3): A non-parametric algorithm that classifies based on nearest neighbors.

Decision Tree (clf4): A tree-based model that splits data based on feature thresholds.

Multi-Layer Perceptron (clf5): A neural network with hidden layers for complex patterns.

Random Forest (clf6): An ensemble of decision trees with bootstrapped samples.

XGBoost (clf7): A gradient boosting framework for boosting decision trees.

AdaBoost (clf8): An ensemble method that combines weak learners.

The ensemble classifier (eclf) combines the predictions from clf6, clf7, and clf8 using a soft voting strategy.

**Usage**

Install the required Python libraries (e.g., scikit-learn, xgboost).

Load your dataset and preprocess it.

Train the individual classifiers (clf1 to clf8).

Create the ensemble classifier (eclf).

Evaluate the ensemble’s performance using cross-validation or a holdout set.



**Model Comparison:**
Eight models were evaluated, and the best-performing one was selected

**Models Evaluated**

*Logistic Regression*

*Naive Bayes*

*K-Nearest Neighbors*

*Decision Tree*

*Neural Network (Multi-Layer Perceptron)*

*Random Forest*

*XGBoost*

*AdaBoost*

**Results**

**ROC_AUC Scores:* The AUC scores range from approximately 0.58 to 0.99, indicating the models’ performance in distinguishing between positive and negative classes.

**Execution Time:* The execution time varies from around 0 to 30 seconds for different models.

**Visualization**

*Some models achieve high AUC scores (e.g., XGBoost), while others perform moderately (e.g., Naive Bayes).

*Execution time varies significantly across models.

*Consider the trade-off between model performance and execution time when choosing a suitable model for your specific use case.
