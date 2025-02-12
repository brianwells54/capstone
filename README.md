### Project Title
**Credit Card Fraud Detection Using Machine Learning**

**Author**  
Brian Wells

#### Executive Summary
This project leverages machine learning to detect fraudulent credit card transactions, aiming to minimize financial losses for banks and protect customers from unauthorized activities. A logistic regression model was implemented to classify transactions as fraudulent or legitimate, balancing precision and recall to reduce false positives while catching most fraud cases.

#### Rationale
Credit card fraud results in significant financial losses for banks and can erode customer trust due to account freezes and transaction disruptions. Detecting fraud early helps prevent unauthorized charges, reduces operational costs, and enhances the customer experience by maintaining account security.

#### Research Question
How can machine learning models be used to detect fraudulent transactions in credit card operations at a financial institution, enabling proactive prevention of financial losses?

#### Data Sources
- **Public Dataset:** [Credit Card Fraud Transaction Data](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) from Kaggle, containing anonymized transaction records labeled as fraudulent or legitimate.

#### Methodology
1. **Data Preprocessing & Cleaning:** Handled missing values, removed inconsistencies, and encoded categorical features.
2. **Feature Engineering:** Created features like **transaction velocity**, **time of day**, and **country mismatch** to improve model performance.
3. **Modeling:** Implemented a **logistic regression** model with balanced class weights to handle data imbalance.
4. **Evaluation:** Assessed model performance using **confusion matrix**, **precision**, **recall**, **F1-score**, and **ROC-AUC** metrics.

#### Results
- The model achieved a **recall of 0.93**, detecting 93% of fraudulent transactions, with a **precision of 0.53**, indicating some false positives.
- The **ROC-AUC score of 0.9745** reflects strong overall performance in distinguishing fraud from legitimate transactions.
- While the model effectively catches most fraud, further tuning is needed to reduce false positives without missing fraudulent activities.

#### Next Steps
1. **Implement Advanced Models:** Use boosting algorithms like **XGBoost** or **LightGBM** to improve detection accuracy.
2. **Enhance Feature Engineering:** Add features like **spending pattern deviations** and **location consistency** for more nuanced fraud detection.
3. **Real-Time Deployment:** Adjust classification thresholds and integrate the model into a **real-time monitoring system** to proactively prevent fraud.

#### Outline of Project
- [Credit Card Fraud Detection Notebook](https://github.com/brianwells54/capstone/blob/main/credit_card_fraud_detection.ipynb)

##### Contact and Further Information
*For inquiries or further details, contact Brian Wells at brian.wells@ndl.cc*
