# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.
2. Upload the dataset and check for any null or duplicated values using .isnull() and .duplicated() function respectively.
3. Import LabelEncoder and encode the dataset.
4. Import LogisticRegression from sklearn and apply the model on the dataset.
5. Predict the values of array.
6. Calculate the accuracy, confusion and classification report by importing the required modules from sklearn.
7. Apply new unknown values
 

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: S.ANUSHARON 
RegisterNumber: 212222240010

import pandas as pd
data=pd.read_csv('/content/Placement_Data (1).csv')
data.head()

data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
data1.head()

data1.isnull().sum()

data1.duplicated().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"] = le.fit_transform(data1["gender"])
data1["ssc_b"] = le.fit_transform(data1["ssc_b"])
data1["hsc_b"] = le.fit_transform(data1["hsc_b"])
data1["hsc_s"] = le.fit_transform(data1["hsc_s"])
data1["degree_t"] = le.fit_transform(data1["degree_t"])
data1["workex"] = le.fit_transform(data1["workex"])
data1["specialisation"] = le.fit_transform(data1["specialisation"])
data1["status"] = le.fit_transform(data1["status"])
data1

x=data1.iloc[:,:-1]
x

y=data1["status"]
y

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size = 0.2,random_state = 0)

from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver = "liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
y_pred


from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy

from sklearn.metrics import confusion_matrix
confusion=(y_test,y_pred)
confusion

from sklearn.metrics import classification_report
classification_report1=classification_report(y_test,y_pred)
print(classification_report1)

lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])

*/
```

## Output:
![4 1](https://user-images.githubusercontent.com/119405600/237018313-00378816-abf2-4d71-9d37-67e49fe4120e.png)

![4 2](https://user-images.githubusercontent.com/119405600/237018324-96d2be7a-dfd6-4e39-9c37-078187436acf.png)

![4 3](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/0cb3d1bc-84d2-44a4-80cd-572f204d166f)

![4 4](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/c119733d-6f0b-4c21-9ea7-9fbc2dee8aef)

![4 5](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/6f6cce4a-f0f5-4ef1-b42c-3bcc04d4391b)

![4 6](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/26f536c6-3b37-4b0b-99f2-597ef390f2c9)

![4 7](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/9bb15e17-e21b-4457-9b31-47d185b90013)

![4 8](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/2ec47f9e-6d7c-4d12-bfa2-0cb280a55b4c)


![4 9](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/f6cce6fa-2110-43f4-96fa-a7e43162a9bb)

![4 10](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/b3a09a21-1c62-45c4-be00-dc1cb1abea04)

![4 11](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/7179e1a2-4914-42af-afb8-675080fad31e)

![4 12](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/adaacdc8-bde2-40e0-a629-352e10f6df5b)

![4 13](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/d033a000-4399-4acd-8ade-94f79bc32956)



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
