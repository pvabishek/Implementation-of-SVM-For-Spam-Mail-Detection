# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
STEP 1: Start
  
STEP 2: Data Loading and Exploration

STEP 3: Data Preparation

STEP 4: Train-Test Split

STEP 5: Text Vectorization

STEP 6: Model Training

STEP 7: Making Predictions

STEP 8: Evaluation

STEP 9: End
## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: ABISHEK PV
RegisterNumber: 212222230003
import pandas as pd
data = pd.read_csv("spam.csv",encoding = 'Windows-1252') 
data.head()
data.isnull().sum()
x = data["v1"].values
y = data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size = 0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
#Countvectorizer is a method to convert text to numerical data.The text is transformed to a sparse data
cv = CountVectorizer()
x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)
from sklearn.svm import SVC
svc = SVC()
svc.fit(x_train,y_train)
y_pred = svc.predict(x_test)
y_pred
from sklearn.metrics import accuracy_score,confusion_matrix,classification_report
acc = accuracy_score(y_test,y_pred)
acc
con = confusion_matrix(y_test,y_pred)
print(con)
cl = classification_report(y_test,y_pred)
print(cl)
*/
```

## Output:
## data.head():
![image](https://github.com/user-attachments/assets/793cdbf1-6982-40b6-b579-664f18455db8)

## data.info():
![image](https://github.com/user-attachments/assets/84e0a36c-cd22-4072-aa6a-88d97401e192)

## y_pred:
![image](https://github.com/user-attachments/assets/39766337-f7d0-4aca-9ae2-09463c744bf7)

## accuracy_score:
![image](https://github.com/user-attachments/assets/ee1c7fa8-f190-4970-8596-dd58e512f78b)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
