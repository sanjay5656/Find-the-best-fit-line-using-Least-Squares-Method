## Implementation of Univariate Linear Regression
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
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: SANJAY S
RegisterNumber: 212221243002

import matplotlib.pyplot as plt
x=[5,6,3,2,6,7,1,2]
y=[2,3,6,5,8,3,5,8]
plt.scatter(x,y)
plt.show()

import numpy as np
import matplotlib.pyplot as plt

#assign input
x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([1,3,2,5,7,8,8,9,10,12])

#mean values of input
x_mean=np.mean(x)
print(x_mean)
y_mean=np.mean(y)
print(y_mean)

num=0
denum=0

for i in range(len(x)):
  num+=(x[i]-x_mean)*(y[i]-y_mean)
  denum+=(x[i]-x_mean)**2

#find m
m=num/denum

#find b
b=y_mean-m*x_mean
print("m",m)
print("b",b)

#find y_pred
y_pred=m*x+b
print(y_pred)

#plot graph
plt.scatter(x,y)
plt.plot(x,y_pred,color='green')
plt.show() 

```

## Output:

![image](https://user-images.githubusercontent.com/115128955/204522372-968e5aa3-6521-4aa9-9f66-d94232af8808.png)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
