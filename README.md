# MSCS_634_ProjectDeliverable2_3


Overview
This deliverable explores three core data mining techniques using a cleaned dataset from Deliverable 1:

Classification using Decision Trees and K-Nearest Neighbors (KNN)

Clustering using K-Means after PCA dimensionality reduction

Association Rule Mining using the Apriori algorithm

 Key Insights
 Classification
Decision Tree and KNN were implemented to classify the Outcome variable.

KNN with hyperparameter tuning (GridSearchCV) achieved better performance, with the best k = {best_k} selected using cross-validation.

ROC-AUC analysis showed that both models had reasonable class separation, with KNN generally performing better in terms of precision and recall.

Clustering
K-Means Clustering was performed on PCA-reduced data to visualize group separations.

Despite using unsupervised learning, the clusters aligned moderately well with class separations, suggesting inherent structure in the data.

Association Rule Mining
Using the Apriori algorithm, strong rules were extracted with:

Minimum Support = 0.3

Confidence ≥ 0.6

These rules highlighted co-occurrence patterns in features (e.g., high glucose levels and BMI often appeared together in certain groups), providing actionable insights into feature relationships.

Practical Relevance
Healthcare Monitoring: Classification models can be used to detect at-risk patients based on clinical features.

Patient Profiling: Clustering can group patients for personalized treatments or lifestyle recommendations.

Risk Factor Analysis: Association rules can inform healthcare providers about commonly co-occurring conditions or symptoms, assisting in early diagnosis or preventive strategies.

Challenges & Solutions
Challenge	Solution
Imbalanced feature scales	Applied StandardScaler to normalize data for KNN
Choosing optimal K for KNN	Used GridSearchCV with 5-fold CV to identify best k
High-dimensional data for clustering	Applied PCA to reduce dimensions before clustering
Sparse binary encoding for Apriori	Used TransactionEncoder and binarized features based on mean

Visual Outputs
Confusion matrices for both classifiers

ROC curves for performance comparison

2D scatter plot of K-Means clusters (PCA-transformed)

Association rules table summarizing key itemsets
