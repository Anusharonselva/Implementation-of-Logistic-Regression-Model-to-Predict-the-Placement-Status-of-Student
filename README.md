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

![Screenshot (287)](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/19271066-1832-4e80-af29-8e26128bb46c)


![Screenshot (287) 1](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/26bd5937-e123-4da8-9aeb-457abdbd6fe3)


![Screenshot (288)](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/157b6da4-55fe-4a52-9fce-b663a1c372ce)

![Screenshot (288) 1](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/468014ac-6c08-43f5-9116-e5701b31ab12)

![Screenshot (289)](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/44fa5649-7306-443f-841f-435a2e275ecb)

![Screenshot (290)](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/783f449f-bafb-499e-be6b-b5ebf514ff88)

![Screenshot (290) 1](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/eba834c0-0590-4354-88a3-b0f661492349)

![Screenshot (290) 2](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/f5c0a80b-ef33-489a-9548-ccf4f4ba7d13)

![Screenshot (290) 3](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/00cef9d4-03ec-4fa3-834d-6b0ad95afdf4)

![Screenshot (291) 1](https://github.com/Anusharonselva/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119405600/4a619135-5e7a-4fa7-aef1-3ca2bad776bb)


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
