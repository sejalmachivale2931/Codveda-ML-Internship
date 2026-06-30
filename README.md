ML-Internship/
│
├── Level_1_Basic/
│   ├── Task_1_Preprocessing/
│   │   └── data_preprocessing.py
│   └── Task_2_Linear_Regression/
│       └── linear_regression.py
│
├── Level_2_Intermediate/
│   ├── Task_1_Decision_Tree/
│   │   ├── decision_tree_churn.py
│   │   ├── tree_unpruned.png
│   │   ├── tree_pruned.png
│   │   ├── accuracy_vs_alpha.png
│   │   ├── feature_importance.png
│   │   ├── pruning_comparison.csv
│   │   ├── churn-bigml-80.csv
│   │   └── churn-bigml-20.csv
│   └── Task_2_KMeans_Clustering/
│       ├── kmeans_clustering.py
│       ├── elbow_plot.png
│       ├── clusters_2d.png
│       └── 4__house_Prediction_Data_Set.csv
│
└── README.md

✅ Level 1 — Basic

Task 1: Data Preprocessing
Dataset: Iris Dataset
StepMethod UsedMissing valuesMean imputationCategorical encodingLabel Encoding (species column)Feature scalingStandardScalerTrain/Test split80/20 split

Task 2: Linear Regression
Dataset: Boston House Prediction Dataset
Built a Linear Regression model using scikit-learn to predict house prices
Interpreted model coefficients to understand feature impact on price

MetricValueR² Score0.67Mean Squared Error (MSE)24.29


✅ Level 2 — Intermediate
Task 1: Decision Trees for Classification
Dataset: Telecom Customer Churn Dataset (BigML)
Training set: churn-bigml-80.csv (2,666 rows)
Testing set: churn-bigml-20.csv (667 rows)
Target: Churn (True/False)


Steps:
Preprocessing — dropped low-signal columns, binary encoded categorical features
Trained an unpruned Decision Tree (baseline)
Visualized tree structure using plot_tree
Pruned using Cost Complexity Pruning (ccp_alpha)
Evaluated on test set using accuracy, F1-score, classification report, confusion matrix

Results:
MetricUnprunedPrunedTree Depth237Leaf Nodes17318Train Accuracy100%95.5%Test Accuracy91.5%95.7%F1-score (Churn)0.710.84

Classification Report (Pruned Tree — Test Set):

              precision    recall  f1-score   support

    No Churn       0.97      0.98      0.97       572
       Churn       0.89      0.79      0.84        95

    accuracy                           0.96       667

Top Features by Importance:
Total day charge
Customer service calls
Total international minutes
International plan

Task 2: K-Means Clustering
Dataset: Boston House Prediction Dataset (506 houses, 14 features)
Steps:
Loaded dataset (whitespace-separated, no header — manually defined column names)
Scaled features using StandardScaler
Applied Elbow Method (k=1 to k=10) to find optimal clusters → k=3 selected
Trained K-Means model (k=3)
Visualized clusters using PCA (14D → 2D scatter plot)
Interpreted cluster characteristics


Cluster Interpretation:

Cluster 0Cluster 1Cluster 2Crime RateHigh (11.05)Low (0.38)Very Low (0.18)Avg RoomsSmall (5.95)Medium (6.09)Large (6.94)House AgeOld (90.7 yrs)Medium (69 yrs)Newer (43 yrs)Avg Price$16,190$21,130$31,630Type🔴 Urban/Low-income🟡 Suburban/Middle-class🟢 Affluent/Premium


🛠️ Tools Used


Python
Pandas
NumPy
Scikit-learn
Matplotlib
Seaborn

⚙️ How to Run

Prerequisites
bashpip install pandas numpy scikit-learn matplotlib seaborn
Level 1
bashpython Level_1_Basic/Task_1_Preprocessing/data_preprocessing.py
python Level_1_Basic/Task_2_Linear_Regression/linear_regression.py
Level 2
bashpython Level_2_Intermediate/Task_1_Decision_Tree/decision_tree_churn.py
python Level_2_Intermediate/Task_2_KMeans_Clustering/kmeans_clustering.py


📌 Key Learnings
Data preprocessing (scaling, encoding, imputation) is a critical first step in any ML pipeline
Pruning is essential for Decision Trees to prevent overfitting and improve generalization
K-Means requires feature scaling — without it, high-range features dominate distance calculations
The Elbow Method helps choose optimal k, though it involves some subjectivity
Unsupervised learning can discover meaningful real-world patterns without labeled data

👩‍💻 Author
Sejal Dilip Machivale
Intern ID: CV/A1/77891
Codveda Technology — Machine Learning Internship
