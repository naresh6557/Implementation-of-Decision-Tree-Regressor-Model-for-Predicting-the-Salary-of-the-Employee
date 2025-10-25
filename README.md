# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas

2.Import Decision tree classifier

3.Fit the data in the model

4.Find the accuracy score

## Program:
```
Naresh kumar R
212224040213
```
```
import pandas as pd
data=pd.read_csv("/content/Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()

y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
```
## Output:

<img width="587" height="262" alt="image" src="https://github.com/user-attachments/assets/3f8a194c-f4ee-4b35-b770-30f888f2fcf1" />

<img width="585" height="437" alt="image" src="https://github.com/user-attachments/assets/e2cd9def-3078-4146-abf7-54b38743b3c2" />

<img width="487" height="251" alt="image" src="https://github.com/user-attachments/assets/61a89f5d-d77c-474e-a9d6-031df541f0db" />

<img width="429" height="90" alt="image" src="https://github.com/user-attachments/assets/e921f269-5b4c-4337-ae92-935779080760" />

<img width="318" height="47" alt="image" src="https://github.com/user-attachments/assets/93135b06-718f-429e-b531-947b6a5273b4" />

<img width="1412" height="69" alt="image" src="https://github.com/user-attachments/assets/7b91b5c0-6043-4ccc-8b1c-f1d1ed058b27" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
