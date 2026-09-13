# Fraud Detection & Risk Scoring System

A machine learning project for detecting fraudulent financial transactions
using the PaySim dataset.

The main goal of this project is to identify fraudulent transactions despite
the dataset being highly imbalanced, and then convert the model's prediction
into a simple risk score.

## What I Built

- Cleaned and prepared the transaction data
- Used a time-based train, validation and test split
- Created features from transaction amount, account balances and transaction history
- Compared different machine learning models
- Handled class imbalance using class weights
- Optimized the classification threshold using validation data
- Generated fraud probability for each transaction
- Converted probability into a 0–100 risk score
- Classified transactions as Low, Medium or High Risk

## Models Used

1. Logistic Regression
2. Random Forest
3. HistGradientBoosting

Random Forest was selected as the final model based on its validation
performance.

## Results

The final Random Forest model was evaluated on the unseen test set.

| Metric | Score |
|---|---:|
| Precision | 100.00% |
| Recall | 99.95% |
| F1-Score | 99.98% |
| ROC-AUC | 100.00% |
| PR-AUC | 100.00% |

The decision threshold was selected using the validation set and was set to
0.45 for the final test evaluation.

## Risk Scoring

The predicted fraud probability is converted into a score between 0 and 100.

| Score | Risk |
|---|---|
| 0–30 | Low Risk |
| 30–70 | Medium Risk |
| 70–100 | High Risk |

For example, a prediction probability of 0.85 gives a risk score of 85,
which is classified as High Risk.

## Dataset

I used the PaySim synthetic financial transaction dataset.

It contains information such as:

- Transaction type
- Transaction amount
- Sender and receiver balances
- Time step
- Fraud label

The dataset is highly imbalanced, with fraudulent transactions making up only
a very small part of the data.

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Structure

```text
fraud-detection-risk-engine/
├── README.md
├── notebook_01_data_understanding.ipynb
├── notebook_02_EDA.ipynb
├── notebook_03_fraud_detection_final.ipynb
└── .gitignore
```
