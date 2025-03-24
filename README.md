### Project Title
**Credit Card Fraud Detection Using Machine Learning**

**Author**  
Brian Wells

---

#### Executive Summary
This project applies supervised machine learning techniques to detect fraudulent credit card transactions, enabling banks to prevent financial losses and protect customers from unauthorized activity. Four classification models were implemented and evaluated: **Logistic Regression**, **Random Forest**, **Decision Tree**, and **XGBoost**. The evaluation emphasizes **recall** to ensure most fraud is detected, while also considering **precision** to reduce false alarms.

---

#### Rationale
Credit card fraud can lead to significant financial and reputational damage for banks. An effective fraud detection system not only minimizes losses but also enhances customer trust by reducing false positives that could result in unnecessary account freezes or declined transactions.

---

#### Research Question
How can supervised machine learning models be used to accurately detect fraudulent transactions in real-time, balancing the tradeoff between false positives and false negatives?

---

#### Data Sources
- **Public Dataset:** [Credit Card Fraud Transaction Data](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) from Kaggle. The dataset includes anonymized features from European credit card transactions, with a highly imbalanced class distribution (fraud cases represent less than 1%).

---

#### Methodology
1. **Data Preprocessing**
   - Cleaned and explored the data.
   - Verified class imbalance and feature distributions.
2. **Feature Engineering**
   - Introduced new features including **transaction velocity** and **hour of day**.
3. **Modeling**
   - Trained four models: **Logistic Regression**, **Random Forest**, **Decision Tree**, and **XGBoost**.
   - Used consistent train-test split for fair comparison.
4. **Evaluation**
   - Evaluated each model using **confusion matrix**, **classification report**, and **ROC-AUC**.
   - Focused on maximizing **recall** while preserving **precision** for fraud cases.

---

#### Results

| Model                 | Precision (Fraud) | Recall (Fraud) | F1-Score (Fraud) | ROC-AUC |
|----------------------|-------------------|----------------|------------------|---------|
| **Logistic Regression** | 0.53                | 0.93           | 0.67             | 0.9745   |
| **Random Forest**       | 0.98                | 0.81           | 0.89             | 0.9901  |
| **Decision Tree**       | 0.78               | 0.83           | 0.80             | 0.9100   |
| **XGBoost**             | 0.96                | 0.83           | 0.89             | 0.9821 |

- **XGBoost** demonstrated good overall performance, with a high ROC-AUC score, tied for the highest F1-Score, and relatively high Precision.
- **Logistic Regression** achieved high recall but suffered from low precision, resulting in a lower F1-score.
- **Decision Tree** seems to have achieved a very efficient cycle time and reasonable overall performance, but was mediocre across the board in comparison to other models.
- **Random Forest** delivered balanced performance and strong ROC-AUC, as well as a high F1-Score, high Precision and relatively high Recall.

- **Random Forest and XGBoost** are both suitable models for this exercise, but I would give the slight edge to Random Forest due to it's higher Precision and AUC scores.  Either model would serve well for Fraud detection.

---

#### Outline of Project
📓 [Credit Card Fraud Detection Notebook](https://github.com/brianwells54/capstone/blob/main/credit_card_fraud_detection.ipynb)

1. **Introduction:** Project motivation and business context.  
2. **Data Loading and Exploration:** Understanding the dataset.  
3. **Data Cleaning:** Verifying integrity and addressing imbalance.  
4. **Exploratory Data Analysis (EDA):** Visualizing key transaction patterns.  
5. **Feature Engineering:** Creating custom fraud-indicative features.  
6. **Modeling:** Implementing and training four classification models.  
7. **Evaluation:** Measuring precision, recall, F1-score, and ROC-AUC.  
8. **Conclusion:** Final model assessment and selection rationale.

---

##### Contact and Further Information
*For inquiries or collaboration, contact Brian Wells at brian.wells@ndl.cc*
