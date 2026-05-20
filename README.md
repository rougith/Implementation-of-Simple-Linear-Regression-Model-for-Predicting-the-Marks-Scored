# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load the dataset into a DataFrame and explore its contents to understand the data structure.

2.Separate the dataset into independent (X) and dependent (Y) variables, and split them into training and testing sets.

3.Create a linear regression model and fit it using the training data.

4.Predict the results for the testing set and plot the training and testing sets with fitted lines.

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by:Rougith D
RegisterNumber:25017014
*/
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
X=np.array([1,2,3,4,5]).reshape(-1,1)
Y=np.array([77,83,87,92,99])
model=LinearRegression()
model.fit(X,Y)
m=model.coef_[0]
b=model.intercept_
print("slope(m):",m)
print("intercept(b):",b)
X_input=float(input("Enter hours studied"))
predicted_marks=model.predict([[X_input]])
print("Predicted Marks:",predicted_marks[0])
Y_pred=model.predict(X)
plt.scatter(X,Y,label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied:")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()

```

## Output:
<img width="744" height="602" alt="{B9FE0150-6644-407C-8F84-961CE3D2972B}" src="https://github.com/user-attachments/assets/e3a940a6-40e4-40ec-9100-ef1c08633418" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
