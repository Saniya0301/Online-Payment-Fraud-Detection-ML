# 💳 Online Payment Fraud Detection using Machine Learning

This project detects fraudulent online payment transactions using **Machine Learning** with a Decision Tree Classifier.  
It uses transaction data to classify whether a transaction is **Fraud** or **No Fraud**.

---

## 📌 Dataset
The dataset contains details of online transactions with the following columns:

| Column Name       | Description |
|-------------------|-------------|
| step              | Time step in hours |
| type              | Type of transaction (`CASH_OUT`, `PAYMENT`, `CASH_IN`, `TRANSFER`, `DEBIT`) |
| amount            | Transaction amount |
| nameOrig          | Customer initiating the transaction |
| oldbalanceOrg     | Initial balance before transaction |
| newbalanceOrig    | New balance after transaction |
| nameDest          | Recipient |
| oldbalanceDest    | Initial balance of recipient |
| newbalanceDest    | New balance of recipient |
| isFraud           | Fraud indicator (`0` = No Fraud, `1` = Fraud) |
| isFlaggedFraud    | Transactions flagged as fraud by rules |

---

## 📊 Exploratory Data Analysis (EDA)

1. **Transaction Type Distribution**
   - Visualized using a **donut pie chart** with Plotly.

2. **Correlation with Fraud**
   - Checked correlation between features and the `isFraud` column.
   - `amount` has the highest correlation with fraud after `isFraud` itself.

---


---

## 🧠 Model Training

**Algorithm Used:** Decision Tree Classifier (`sklearn.tree.DecisionTreeClassifier`)

**Features Used:**
- `type`
- `amount`
- `oldbalanceOrg`
- `newbalanceOrig`

**Train-Test Split:**
```python
train_test_split(test_size=0.20, random_state=42)

---
🏷 License

This project is open-source under the MIT License.

---
Author

Saniya Chhabra
