# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.To implement the linear regression using the standard libraries in the python.
2.Use slicing function() for the x,y values.
3.Using sklearn library import training , testing and linear regression modules.
4.Predict the value for the y.
5.Using matplotlib library plot the graphs.
6.Use xlabel for hours and ylabel for scores.
7.End the porgram.


## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Nithya shree.B
RegisterNumber:  21222320071
*/
import numpy as np
import matplotlib.pyplot as plt

#Preprocessing Input data

X = np.array(eval(input()))
Y = np.array(eval(input()))

# Mean
X_mean =np.mean(X)
Y_mean =np.mean(Y)
num=0 #for slope
denom=0 #for slope

#to find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
     num+=(X[i] -X_mean)*(Y[i]-Y_mean)
     denom+= (X[i]-X_mean)**2

#calculate slope
m=num/denom

#calculate intercept
b=Y_mean-m*X_mean

print(m,b)
#Line equation
y_predicted=m*X+b
print(y_predicted)

#to plot graph
plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.show()
```

## output:
![alt text](<Screenshot 2024-03-06 105707.png>)
![alt text](<Screenshot 2024-03-06 105719.png>)


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
