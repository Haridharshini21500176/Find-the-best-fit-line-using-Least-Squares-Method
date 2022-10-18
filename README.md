# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: S.Haridharshini
RegisterNumber:  212221230033
*/
import matplotlib.pyplot as plt 
x=[5,6,3,2,6,7,1,2]
y=[2,3,6,5,8,3,5,8]
plt.scatter(x,y); 
plt.plot(x,y) 
plt.show() 

# LEAST SQUARE METHOD
import numpy as np
import matplotlib.pyplot as plt
X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])
X_mean=np.mean(X)
print(X_mean)
Y_mean=np.mean(Y)
print(Y_mean)
num=0
denum=0
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2
m=num/denum
print(m)
b=Y_mean - m*X_mean
print(b)
Y_pred=m*X+b
print(Y_pred)
plt.scatter(X,Y,color='purple')
plt.plot(X,Y_pred,color='red') 
plt.show() 

```


## Output:
![193417751-9664305a-35c3-48e1-a689-8782af7e0b02](https://user-images.githubusercontent.com/94168395/196486843-06c7b4be-66a5-4f4a-b367-fe915077136f.png)
![193417761-3d6d6d18-cdb6-4e12-893f-881ca6225fd8](https://user-images.githubusercontent.com/94168395/196486882-e809b3fa-c461-475b-bc29-350b27f7f9fc.png)
![193417779-62bcd821-ae50-4beb-8b89-078c7c92a7dd](https://user-images.githubusercontent.com/94168395/196486926-9160f25c-6ee7-407f-bb8f-d5af5ede1107.png)
![193417780-903892ed-7b54-4a9a-bef4-2f5eceda8486](https://user-images.githubusercontent.com/94168395/196487016-e7a0c32f-a583-4651-8d0c-fda5be4757a0.png)
![193417745-0b31710e-9afa-4e36-9314-954a7ee698a7](https://user-images.githubusercontent.com/94168395/196487051-86286cde-ca54-4a7e-9b1d-0fd1f089f2c9.png)



## GRAPH:
![193417790-b2ecd529-c062-495e-b092-e2542c33db97](https://user-images.githubusercontent.com/94168395/196487101-9b85560b-8a5b-42fe-94ae-b2a1fceb1ef3.png)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
