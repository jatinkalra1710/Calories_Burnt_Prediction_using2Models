# 🔥 Calories Burnt Prediction Using ML & XGBoost

## 📌 Overview
This project aims to predict the number of calories burnt during physical activity using demographic and biometric data. It compares the performance of **Linear Regression** and **XGBoost Regressor**, showcasing the power of ensemble methods in regression tasks.

## 📂 Dataset
- Source: [Kaggle Calories Burnt Dataset](https://www.kaggle.com/datasets)
- File used: `calories.csv`
- Features include:
  - `User_ID`, `Gender`, `Age`, `Height`, `Weight`, `Duration`, `Heart_Rate`, `Body_Temp`
  - Target: `Calories`

## 🧼 Data Preprocessing
- Checked for missing and duplicate values
- Encoded `Gender` using `LabelEncoder`
- Dropped `User_ID` and `Calories` from feature set
- Visualized correlations using `seaborn.heatmap`
- Distribution plot for `Age` using `sns.distplot`

## 🧪 Model Training
Two models were trained and evaluated:
- **Linear Regression**
- **XGBoost Regressor**

### 🔧 Train-Test Split
```python
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size=0.2, random_state=46)
```

## 📊 Evaluation Metrics
| Model              | R² Score | Mean Absolute Error |
|-------------------|----------|----------------------|
| Linear Regression | 0.9667   | 8.54                 |
| XGBoost Regressor | 0.9989   | 1.39                 |

✅ **XGBoost significantly outperforms Linear Regression**, indicating its strength in capturing non-linear relationships and feature interactions.

## 📈 Visualizations
- Correlation heatmap for feature relationships
- Age distribution plot for demographic insights

## 🧠 Future Enhancements
- Hyperparameter tuning for XGBoost
- Feature scaling and normalization
- Integration with real-time fitness tracking data
- Deployment as a REST API for mobile fitness apps
