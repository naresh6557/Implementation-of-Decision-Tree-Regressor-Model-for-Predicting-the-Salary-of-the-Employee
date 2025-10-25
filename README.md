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
SANJAY KUMAR B
212224230242
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

<img width="1116" height="314" alt="image" src="https://github.com/user-attachments/assets/60595980-1de2-4ca2-ad85-612fc6a1de6a" />

<img width="1164" height="232" alt="image" src="https://github.com/user-attachments/assets/e06c2bcd-f4a5-4f0e-85b2-8c022f4a9e30" />

<img width="1189" height="206" alt="image" src="https://github.com/user-attachments/assets/5c1b799f-1cfb-43dd-b877-6e4c6c2ab7ab" />

<img width="1005" height="256" alt="image" src="https://github.com/user-attachments/assets/9b0a1779-8ebd-4710-bdce-b3099072f076" />

<img width="1059" height="255" alt="image" src="https://github.com/user-attachments/assets/4cbdc398-a2c7-467f-bdcc-ce24f9c72053" />

<img width="1026" height="35" alt="image" src="https://github.com/user-attachments/assets/9e6c74e1-63c7-4282-b4da-4cff20cc3188" />

<img width="838" height="38" alt="image" src="https://github.com/user-attachments/assets/5600731a-b534-4f0a-867b-6a7476a12a27" />

<img width="1517" height="109" alt="image" src="https://github.com/user-attachments/assets/df9761bf-6935-49f3-8b84-0c3ff1efd15e" />

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
