# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and create the dataset.

2. Select the input features and target variable.

3. Split the dataset into training data and testing data.

4. Train the SGD Classifier model using training data.

5. Predict the test data results and find the accuracy of the model.


## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Ranjani S
RegisterNumber: 212225230224

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import SGDClassifier
from sklearn.metrics import accuracy_score
from sklearn.preprocessing import StandardScaler

# Dataset
data = {
    'Age': [25, 30, 45, 35, 22, 40, 28, 50, 23, 31],
    'Salary': [40000, 50000, 80000, 60000, 35000, 90000, 45000, 100000, 30000, 52000],
    'Years': [1, 5, 10, 7, 2, 12, 3, 15, 1, 6],
    'Churn': [1, 0, 0, 0, 1, 0, 1, 0, 1, 0]
}

# Create DataFrame
df = pd.DataFrame(data)

# Features and Target
X = df[['Age', 'Salary', 'Years']]
y = df['Churn']

# Split data
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=1
)

# Scaling
sc = StandardScaler()
X_train = sc.fit_transform(X_train)
X_test = sc.transform(X_test)

# SGD Classifier Model
model = SGDClassifier(random_state=1)
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)

# Accuracy
print("Accuracy:", accuracy_score(y_test, y_pred))

# Plot
plt.plot(y_test.values)
plt.plot(y_pred)
plt.title("SGD Classifier")
plt.show() 
*/
```

## Output:

<img width="741" height="472" alt="image" src="https://github.com/user-attachments/assets/4fbd8920-e46a-4657-9b90-7a465f2083e5" />


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
