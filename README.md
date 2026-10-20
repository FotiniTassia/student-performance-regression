# Student Performance Prediction: A Data Integrity Case Study

## 🎯 Project Objective
"The main goal of this project was to demonstrate how deduplication impacts model metrics via row memorization."

## 🔍 Key Engineering Insights
* **The Vulnerability:** Identified **127 duplicate rows** introduced during the synthetic data generation process.
* **The Leakage:** Prior to deduplication, the random `train_test_split` allowed identical rows into both the training and testing sets, artificially inflating model evaluation metrics through row memorization.
* **The Outcome:** Removing duplicate rows dropped the final R² score slightly but established a statistically honest, reliable evaluation baseline.

## 📊 Visualizing the Data Leakage
The side-by-side residual plots embedded within the notebook demonstrate how the error distributions stabilized once identical rows were eliminated, shifting from memorized clusters to an honest baseline evaluation.

## 🛠️ Tech Stack & Workflow
* **Language:** Python 3.14.2
* **Machine Learning:** Scikit-Learn (`LinearRegression`, `train_test_split`)
* **Data & Visualization:** Pandas, NumPy, Matplotlib
* **Environment:** Kaggle Notebook Cloud Architecture
