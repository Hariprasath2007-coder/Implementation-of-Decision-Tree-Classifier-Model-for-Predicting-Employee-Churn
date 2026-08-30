# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Create a dataset containing employee details and churn status.

2.Separate the input features (X) and target variable (y).

3.Split the dataset into training and testing sets.

4.Create and train a Decision Tree Classifier using the training data.

5.Predict employee churn for the test data and calculate the accuracy.

## Program:

```
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import accuracy_score

# Employee data
# Features: Age, Salary, Years at Company
X = [
    [25, 30000, 1],
    [30, 40000, 3],
    [35, 50000, 5],
    [40, 60000, 8],
    [45, 70000, 10],
    [28, 35000, 2],
    [32, 45000, 4],
    [38, 55000, 7],
    [50, 80000, 12],
    [26, 32000, 1]
]

# Churn: 1 = Yes, 0 = No
y = [1, 1, 0, 0, 0, 1, 1, 0, 0, 1]

# Split the dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Create Decision Tree Classifier
model = DecisionTreeClassifier(random_state=42)

# Train the model
model.fit(X_train, y_train)

# Predict churn
y_pred = model.predict(X_test)

# Display predictions
print("Actual Churn:", y_test)
print("Predicted Churn:", y_pred)

# Calculate accuracy
accuracy = accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)

```

## Output:

<img width="662" height="283" alt="image" src="https://github.com/user-attachments/assets/91ca97a5-16b9-4658-b14b-50108424fd8d" />


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
