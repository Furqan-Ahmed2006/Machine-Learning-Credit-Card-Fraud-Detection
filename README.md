Credit Card Fraud Detection

This project focuses on detecting fraudulent credit card transactions using machine learning. The main challenge in this dataset was the extreme class imbalance, where almost all transactions were normal and only a very small portion were fraud.

📌 Project Files

fraud_eda.ipynb – Exploratory Data Analysis

fraud_model_training.ipynb – Model training + Confusion Matrix

fraud_report.docx – 2-page project report

Cleaned Dataset – Saved after EDA

README.md – (This file)

🔍 About the Dataset

Total rows: ~284,000

Features: Time, V1–V28 (PCA components), Amount

Target:

0 = Normal transaction

1 = Fraud transaction

Fraud cases ≈ 0.17% only

This imbalance is the main reason accuracy is not used as an evaluation metric.

🧪 What I Did in This Project
1. Data Cleaning & EDA

Checked missing values

Checked duplicates

Visualized class imbalance

Did not remove outliers (because fraud itself behaves like an outlier)

2. Created a Smaller but Still Imbalanced Dataset

Kept all fraud rows

Sampled 30,000 normal rows

Combined them → easier to train & still realistic

3. Model Training

I trained two models:

Random Forest

XGBoost

Both models were tested using a Confusion Matrix, since accuracy is useless here.

📊 Why Confusion Matrix Matters

In fraud detection, the most important metric is:

Recall (Class 1 – Fraud)

Because missing a fraud transaction (False Negative) is much worse than marking a normal transaction by mistake.

The confusion matrix helped me understand:

Fraud correctly detected (True Positives)

Fraud missed (False Negatives)

Normal transactions flagged wrongly (False Positives)

📈 Results

Both Random Forest and XGBoost performed well, with good recall for the fraud class.
The confusion matrix visualizations are included inside the training notebook.

💡 What I Learned

How to handle real-world imbalanced data

Why accuracy is not reliable for such problems

Importance of confusion matrix and recall

How to sample data without losing important fraud cases

Basics of training ML models on structured data

🛠 Technologies Used

Python
Pandas
Matplotlib / Seaborn
Scikit-Learn
XGBoost
Jupyter Notebook
