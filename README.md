# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary python libraries to perform the decision tree for regression problems.
2. Use pandas library of read.csv to read the csv file.
3. Use X as independent variable and y as dependent variable.
4. Use decision tree regressor to solve the regression problems
5. Use y_pred and use predict the future outcomes.
6. Print the predicted variable (y_pred).
7. Use sklearn.metrics to impore r2_score to get the performance score of the model.
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Harish R
RegisterNumber:  212224230085
*/
```
```
 import pandas as pd
 data=pd.read_csv("/Salary.csv")
 data.head()
 data.info()
 data.isnull().sum()
 from sklearn.preprocessing import LabelEncoder
 le=LabelEncoder()
 data["Position"]=le.fit_transform(data["Position"])
 data.head()
 x=data[["Position","Level"]]
 x.head()
 y=data["Salary"]
 y.head()
 from sklearn.model_selection import train_test_split
 x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
 from sklearn.tree import DecisionTreeRegressor
 dt=DecisionTreeRegressor()
 dt.fit(x_train,y_train)
 y_pred=dt.predict(x_test)
 y_pred
 from sklearn.metrics import r2_score
 r2=r2_score(y_test,y_pred)
 r2
 dt.predict([[5,6]])
```

## Output:

![Screenshot 2025-04-28 190633](https://github.com/user-attachments/assets/0baf4865-4967-4a16-8134-94e20055d822)

![Screenshot 2025-04-28 190649](https://github.com/user-attachments/assets/7156d11d-be73-4459-8219-49ba9615528e)

![Screenshot 2025-04-28 190701](https://github.com/user-attachments/assets/07c77e72-ab29-48dd-83c9-3565f5e0d0bd)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
