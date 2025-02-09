
# [Credit Card Fraud Detection](credit_card_fraud_detection.ipynb)
## Overview
Credit card fraud leads to financial losses for banks and trust issues for customers whose accounts are compromised. Fraudsters exploit weaknesses in transaction systems, making unauthorized purchases that can go undetected, resulting in chargebacks and reimbursement costs for banks. For customers, fraud causes account freezes, disrupted transactions, and stress from resolving disputes. This model aims to proactively detect fraudulent transactions, minimizing financial risks for banks and reducing customer inconvenience. By accurately identifying fraud, the model helps maintain customer trust while balancing caution to avoid false alarms that could affect legitimate transactions.---

## Data Preparation
- **Dataset**: `CreditCardData.csv`
- **Target Variable**: `Fraud` (binary: 1 for "Fraud", 0 for "Legitimate")
- **Features**:
  - These are all the variables that the model will use to predict fraud (e.g., transaction amount, time of day, merchant group)
  - A new feature called 'Time of Day' is being created based on the transaction time, categorizing transactions into Morning, Afternoon, Evening, or Night. This categorization is then used to encode to numerical values
  - A feature called 'Country Mismatch' is created to flag transactions where the 'Country of Transaction' differs from the 'Country of Residence'.
- **Preprocessing**:
  - LabelEncoder is being used to convert categorical features into numerical values

---

## Methodology
 **Model Training and Evaluation**:
   - Logistic Regression was chosen as the initial model.
   - Models were trained on 70% of the data and evaluated on 30%.
   - Confusion matrices were generated to visualize the performance for each model.


---



- **Logistic Regression**:
  - Performed well overall with a balance between training and testing accuracy.

---

## Confusion Matrix Insights
Confusion matrices revealed:
- Confusion Matrix: The model correctly identified 26,032 legitimate transactions. This is a good represenations of non-fraud activity being correctly identified.
- The model mistakenly flagged 1,804 legitimate transactions as fraud. This could lead to customer complaints, but may be better than the alternative.
- The model missed 159 fraudulent transactions, predicting them as legitimate. This number is low, but could cost the bank money.
- The model correctly identified 1,999 fraudulent transactions. These true positives represent an excellent result.


---

## Recommendations
   
1. **Implement Advanced Models (Boosting Algorithms):**:
   - Use algorithms like XGBoost or LightGBM to improve fraud detection accuracy. These models handle complex patterns better than logistic regression and can enhance precision without sacrificing recall..

2. **Enhance Feature Engineering**:
   - Introduce features like transaction velocity (number of transactions in a short period), location consistency (flagging transactions from unusual locations), and spending pattern deviations to improve the model’s ability to detect subtle fraud patterns.

3. **Adjust Thresholds and Monitor in Real-Time**:
   - Fine-tune the classification threshold to balance false positives and false negatives based on business priorities. Implement the model in a real-time fraud detection system and continuously monitor performance with live transaction data for ongoing optimization..

---
