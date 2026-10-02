# Telecom Customer Churn Prediction

## Project Overview 

This projects uses Machine Learning to predict customer churn for a telecom company. A Logistic Regression model was developed using Scikit-learn to classify whether a customer is likely to leave the service. The model was evaluated using **Accuracy** and **Precision**, with a particular focus on **Precision** because false positive predictions may result in unnecessary customer retention costs.

---

## 🎯Objectives
 
- Load and explore customer data
- Preprocess the dataset
- Split data into training and testing sets
- Train a Logistic Regression model
- Evaluate performance using:
- Accuracy
- Precision
- Discuss possible improvements
 
---
 
## ⚒️Technologies Used
 
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotib
 
---
 
## ⚙️Machine Learning Workflow
 
### 1. Data Loading
 
The telecom customer dataset was loaded into a Pandas DataFrame.
 
### 2. Data Preprocessing

 Data preparation included:
- Handling missing values where necessary
- Encoding ategorical variables
- Scaling numerical features using StandardScaler
 
### 3. Train/Test Split
 
The dataset is split into training and testing sets using an 80/20 ratio.
 
### 4. Model Training
 
A Logistic Regression classifier is trained on the training data.
 
### 5. Model Evaluation
 
Model performance is measured using:
 
- Accuracy Score
- Precision Score
- Confusion Matrix
 
---

### Model Performance and Intepretation

The Logistic Regression model achieved an accuracy of **65%**, meaning it correctly predicted customer outcomes 65% of the time. 

However, the precision score was **0.00**, indicating that the model failed to correctly identify customers who were likely to churn.
 
Although the accuracy appears reasonable, the precision score reveals that the model is not effective at identifying true churn cases.

---

## 📊Confusion Matrix Analysis

Because the model did not correctly identify any churning customers, the precision score is **0.00**. This indicates that the model is heavily biased toward predicting the majority class and fails to recognise churn behaviour effectively.

---

<img width="498" height="455" alt="image" src="https://github.com/user-attachments/assets/0d023400-902e-47be-9255-d66fa2ecd20f" />

---

## 💎Why Precision Matters
 
In telecom churn prediction, a false positive occurs when a customer is predicted to churn but would have remained with the company.

False positives can result in:
 
- Unnecessary retention offers
- Discount costs
- Additional marketing expenses
- Reduced profitability

For this reason, precision is particularly important because it measures how reliable churn predictions are.
 
A high precision score allows the company to target retention efforts more effectively and avoid wasting resources on customers who are unlikely to leave.

---
 
## 🚀Potential Model Improvements

If precision remains low, the following techniques may improve model performance:

1. Hyperparameter tuning using GridSearchCV.
2. Addressing class imbalance using SMOTE or class weighting.
 
---
 
## ⚠️Limitation
 
Logistic Regression assumes a linear relationship between features and the target variable.
 
More complex customer behaviour may not be captured effectively.
 
### Alternative Model
 
**Random Forest Classifier** can model non-linear patterns and feature interactions more effectively than Logistic Regression.

---

## 🔮Future Enhancements
- Compare Logistic Regression with Random Forest
- Perform Feature Engineering
- Apply Cross Validation
- Generate ROC and Precision-Recall Curves
- Build a Streamlit Dashboard
- Create interactive Power BI visualisations

---

## 📚Requirements

Install dependencies:

```bash
pip install -r requirements.txt
```

```txt
pandas
numpy
scikit-learn
```

---

## ▶️Running the Project

Run the Python script:

```bash
python churn-prediction.ipynb
```

The program will:
1. Load the dataset
2. Preprocess the data
3. Train the Logistic Regression model
4. Generate predictions
5. Calculate Accuracy and Precision
6. Display the Confusion Matrix
