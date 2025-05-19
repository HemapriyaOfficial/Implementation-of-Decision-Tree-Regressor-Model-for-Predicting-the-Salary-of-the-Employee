# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the standard libraries.

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset.

4.Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

5.Predict the values of arrays.

6.Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7.Predict the values of array.

8.Apply to new unknown values.

## Program:
```
Developed by: HEMAPRIYA K
RegisterNumber:212223040066

import pandas as pd


data = pd.read_csv("Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()

x = data[["Position", "Level"]]
y = data["Salary"]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2)

from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred = df.predict(x_test)

from sklearn import metrics
mse = metrics.mean_squared_error(y_test, y_pred)
mse

r2 = metrics.r2_score(y_test, y_pred)
r2

dt.predict([[5,6]])

```

## Output:

![435885624-28a58f47-35f5-4cfb-b7b7-074fb2b48eab](https://github.com/user-attachments/assets/b1efc9eb-ef53-4920-ad9d-80b4a7a228f9)


![435885682-0a26effa-d8ff-470d-b897-44c9c92f22d4](https://github.com/user-attachments/assets/03528ebe-b147-4e71-ba95-886d537623f6)


![435885865-be432b7b-a8da-460b-a659-343b731ef987](https://github.com/user-attachments/assets/02d75b41-9698-4070-90e2-2df07df882f2)

![435885900-edb39a11-39b2-4e17-8795-c8c1449185bc](https://github.com/user-attachments/assets/0f353471-2d13-4a3b-bb23-ad9c4984dc08)


![435885931-c7033ed4-4573-475b-8322-4f1aa7d9269a](https://github.com/user-attachments/assets/ff7f8909-d0e2-4d2e-8e18-7d71c3d01613)


![435885961-d0a31a7f-2afc-4b3f-84b1-7e8699d44708](https://github.com/user-attachments/assets/25fa0550-033d-485f-8902-cd67cf9444e9)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
