Implementation of Univariate Linear Regression
AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

Equipments Required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Jupyter notebook
Algorithm
Get the independent variable X and dependent variable Y.
Calculate the mean of the X -values and the mean of the Y -values.
Find the slope m of the line of best fit using the formula.
image

4. Compute the y -intercept of the line by using the formula:
image

5. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the scatterplot.
Program:
Program to implement univariate Linear Regression to fit a straight line using least squares.

Developed by:M.Mano

RegisterNumber:212221040100

import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input()))
y=np.array(eval(input()))
x_mean=np.mean(x)
y_mean=np.mean(y)
num,denum=0,0
for i in range(len(x)):
  num+=(x[i]-x_mean)*(y[i]-y_mean)
  denum+=(x[i]-x_mean)**2
m=num/denum
b=y_mean-m*x_mean
print("Slope=",m)
print("\n",b)
y_predicted=m*x+b
print(y_predicted)
y_predict1=m*3+b
print("if x=3:",y_predict1)
plt.scatter(x,y)
plt.plot(x,y_predicted,color='blue')
plt.show()
Output:
GitHub Logo

Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.

