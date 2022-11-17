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
```
```

#import files
import numpy as np
import matplotlib.pyplot as plt

#assign input

X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])


# mean values of input

X_mean=np.mean(X)
print("X_mean =",X_mean)
Y_mean=np.mean(Y)
print("y_mean =",Y_mean)

num=0
denum=0

for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2

# find m
print("find m")
m=num/denum
print("m=",m)

# find b
print("find b")
b=(Y_mean)-(m*X_mean)
print("b =",b)

# find Y_pred
print("find Y_pred")
Y_pred=m*X+b
print("Y_pred =",Y_pred)

#plot graph

plt.scatter(X,Y,color='orange')
plt.plot(X,Y_pred,color='maroon')
print("Graph")
plt.show()
```


## Output:
![193613013-4e3d2bc7-9505-4f68-bb13-28ee00f5f9a8](https://user-images.githubusercontent.com/94168395/202352755-d3c4b610-f5d2-4ae0-97ad-cfbacb48ed1a.png)

![193613026-2ffe5b21-ed00-4aef-8305-f5feab447df5](https://user-images.githubusercontent.com/94168395/202352781-ac768463-4c0f-47b8-a875-bc1896f7ecff.png)

![193613051-68df252f-1267-4c8f-b2fa-432b5c326c2a](https://user-images.githubusercontent.com/94168395/202352795-e1cac91b-15ed-409d-8788-6aa958604639.png)
![193613077-15db6000-7300-40ee-a29e-ebccdb546fca](https://user-images.githubusercontent.com/94168395/202352825-82dec2ce-1672-4215-b5d0-8b07b0dc2915.png)

![193613106-a1ac29f1-3ec3-4962-954b-9ed85bf49d83](https://user-images.githubusercontent.com/94168395/202352853-a00e8d63-b97f-4262-a64c-7e5125d7bbda.png)

![193613139-f9159234-9151-4e7e-8afd-211991118247](https://user-images.githubusercontent.com/94168395/202352876-e194ff05-117c-485e-acbd-e882508b9fda.png)
![193613175-925b8589-41e6-4b92-9650-853523b764b4](https://user-images.githubusercontent.com/94168395/202352892-4fe33e68-ebaf-4323-94d5-ee19918ff1ea.png)

![193613301-118c9cd3-6404-4052-bb08-985cb6cd6809](https://user-images.githubusercontent.com/94168395/202352926-4be7c465-31f9-4d8c-83da-ad51640bf5e7.png)
![193613335-bdd987d5-0e4b-4683-82cb-783c20506f58](https://user-images.githubusercontent.com/94168395/202352960-7d49d6dd-0e7b-4e84-972c-651b171f615d.png)

![193613379-303fc62d-baf1-4b42-93b6-76b2bf4ed3a1](https://user-images.githubusercontent.com/94168395/202352978-2208adb5-dc95-46d4-a65c-88b8ad3834f8.png)
![193613400-02767aa0-2472-4e01-a7f0-6aea82a20e3f](https://user-images.githubusercontent.com/94168395/202352994-396e6942-a3b3-4a00-9b11-b04d3d763d58.png)

## GRAPH:
![193613513-0e562af1-f57a-4dee-b325-8c2c46c46405](https://user-images.githubusercontent.com/94168395/202353068-fa643d5f-d444-4769-b2c4-17f83cdd9938.png)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
