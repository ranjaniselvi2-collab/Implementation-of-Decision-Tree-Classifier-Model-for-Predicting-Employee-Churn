# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries such as Pandas, Matplotlib, and sklearn.

2.Load the dataset and define features (X) and target (y).

3.Split the dataset into training and testing sets.

4.Train the Decision Tree Classifier model.

5.Predict the output and evaluate accuracy.

6.Visualize the Decision Tree using plot_tree().


## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Ranjani S
RegisterNumber: 212225230224

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.metrics import accuracy_score, classification_report

# Employee dataset
data = {
    'Experience': [1, 3, 5, 7, 2, 10, 4, 8, 6, 9],
    'MonthlyHours': [160, 170, 180, 200, 150, 220, 175, 210, 190, 230],
    'Projects': [2, 3, 5, 6, 2, 8, 4, 7, 5, 9],
    'Churn': [1, 1, 0, 0, 1, 0, 1, 0, 0, 0]
}

# Create DataFrame
df = pd.DataFrame(data)

# Features and Target
X = df[['Experience', 'MonthlyHours', 'Projects']]
y = df['Churn']

# Train-Test Split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Create Decision Tree Classifier
model = DecisionTreeClassifier(random_state=42)

# Train the model
model.fit(X_train, y_train)

# Predict the test data
y_pred = model.predict(X_test)

# Model Evaluation
print("Accuracy:", accuracy_score(y_test, y_pred))

print("\nClassification Report:\n")
print(classification_report(y_test, y_pred))

# Decision Tree Diagram
plt.figure(figsize=(12, 6))

plot_tree(
    model,
    feature_names=['Experience', 'MonthlyHours', 'Projects'],
    class_names=['No Churn', 'Churn'],
    filled=True
)

plt.title("Decision Tree for Employee Churn Prediction")
plt.show()
```

## Output:
<img width="1128" height="747" alt="Screenshot 2026-05-19 143012" src="https://github.com/user-attachments/assets/ebf1f9c2-bbf4-48bd-a6cf-4e53fb1c3c94" />


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
