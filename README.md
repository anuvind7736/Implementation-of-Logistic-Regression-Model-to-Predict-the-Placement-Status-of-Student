# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
step 1 - Start program.

step 2 - Import the required packages and print the present data.

step 3 - Print the placement data and salary data.

step 4 - Find the null and duplicate values.

step 5 - Using logistic regression find the predicted values of accuracy , confusion matrices.

step 6 - Display the results.

step 7 - End program.

## Program:
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: ANUVIND KRISHNA.K
RegisterNumber:  212223080004
import pandas as pd
data=pd.read_csv("Placement_Data.csv")
data.head()

data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)#Browses the specified row or column
data1.head()

data1.isnull().sum()

data1.duplicated().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"] )     
data1["status"]=le.fit_transform(data1["status"])       
data1 

x=data1.iloc[:,:-1]
x

y=data1["status"]
y

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
y_pred

from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy

from sklearn.metrics import confusion_matrix
confusion=confusion_matrix(y_test,y_pred)
confusion

from sklearn.metrics import classification_report
classification_report1 = classification_report(y_test,y_pred)
print(classification_report1)

lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])
*/

## Output:
ACCURACY SCORE :

![image](https://github.com/user-attachments/assets/60984f87-7e3b-45a0-a8b4-4c3f5c386577)

CONFUSION MATRIX:

![image](https://github.com/user-attachments/assets/a4767edf-cf35-448a-bf2a-65177f0697d1)

CLASSIFICATION REPORT:

![image](https://github.com/user-attachments/assets/302bb28b-e979-4fa7-876c-4ca5c4e2acfa)

GRAPH:

![image](https://github.com/user-attachments/assets/cd54c4d0-f369-4eef-b00d-545e0ac723b8)
## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
