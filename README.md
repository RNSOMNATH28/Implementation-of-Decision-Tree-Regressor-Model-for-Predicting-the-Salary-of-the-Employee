# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. Calculate Mean square error,data prediction and r2. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: R.N.SOMNATH
RegisterNumber: 212224240158

import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
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



*/
```

## Output:
### Data Head:

<img width="352" height="237" alt="m91" src="https://github.com/user-attachments/assets/74789af2-25f9-40b3-aad7-fe9a7e4c08f2" />


### Data Info:

<img width="422" height="236" alt="m92" src="https://github.com/user-attachments/assets/034114df-7aca-4940-bbc3-4ca457e22efb" />


### isnull() sum():

<img width="218" height="106" alt="m93" src="https://github.com/user-attachments/assets/7e3557fe-6015-4e25-b953-0fe64691c21a" />


### Data Head for salary:

<img width="330" height="232" alt="m94" src="https://github.com/user-attachments/assets/bd781558-a7eb-418d-92b9-d4cea8d714d6" />


### Mean Squared Error :

<img width="162" height="35" alt="m95" src="https://github.com/user-attachments/assets/4180c2cb-42ca-4964-ae10-a993a83f485a" />


### r2 Value:

<img width="243" height="41" alt="m961" src="https://github.com/user-attachments/assets/a3eec29a-b06e-43f6-af5a-c34dd1648e71" />


### Data prediction :

<img width="181" height="23" alt="m96" src="https://github.com/user-attachments/assets/93348c83-550d-46a7-aa01-a966b47974fe" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
