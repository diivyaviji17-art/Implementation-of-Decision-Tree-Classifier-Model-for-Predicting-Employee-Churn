# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: R.Divyadharshini
RegisterNumber: 212225230062
import pandas as pd
data = pd.read_csv("Employee.csv")
print("data.head():")
print(data.head())
print("data.info():")
print(data.info())
print("isnull() and sum():")
print(data.isnull().sum())
print("data value counts():")
print(data["left"].value_counts())
data.columns = data.columns.str.strip()
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["salary"] = le.fit_transform(data["salary"])
data["Departments"] = le.fit_transform(data["Departments"])
print("data.head() after encoding:")
print(data.head())
x = data[[
    "satisfaction_level",
    "last_evaluation",
    "number_project",
    "average_montly_hours",
    "time_spend_company",
    "Work_accident",
    "promotion_last_5years",
    "Departments",
    "salary"
]]

print("x.head():")
print(x.head())
y = data["left"]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(
    x, y, test_size=0.2, random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train, y_train)
y_pred = dt.predict(x_test)
from sklearn import metrics
accuracy = metrics.accuracy_score(y_test, y_pred)
print("Accuracy value:", accuracy)
print("Data Prediction:")
print(dt.predict([[0.5, 0.8, 9, 260, 6, 0, 0, 2, 1]]))
from sklearn.tree import plot_tree
import matplotlib.pyplot as plt
plt.figure(figsize=(12,8))
plot_tree(dt, feature_names=x.columns, class_names=['Stayed', 'Left'], filled=True)
plt.show()
 
*/
```

## Output:
<img width="1239" height="570" alt="Screenshot 2026-03-17 200657" src="https://github.com/user-attachments/assets/3969f70c-7a9d-4bea-9bcd-713d80983385" />
<img width="1131" height="429" alt="Screenshot 2026-03-17 200747" src="https://github.com/user-attachments/assets/1b5468e3-ee9f-43b4-937f-1e3e4a404b45" />
<img width="1067" height="513" alt="Screenshot 2026-03-17 200823" src="https://github.com/user-attachments/assets/a0fd4b48-c87a-4858-8f04-0b2bb3085604" />
<img width="1250" height="602" alt="Screenshot 2026-03-17 200848" src="https://github.com/user-attachments/assets/553b7caa-7d0b-4a94-be57-f72062da4ab2" />
<img width="1222" height="606" alt="Screenshot 2026-03-17 200903" src="https://github.com/user-attachments/assets/70e10ad1-58c6-49d4-8503-9c79e8acfecb" />
<img width="1260" height="789" alt="Screenshot 2026-03-17 200927" src="https://github.com/user-attachments/assets/e136e461-6da2-41e7-bb53-575491a061e8" />




## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
