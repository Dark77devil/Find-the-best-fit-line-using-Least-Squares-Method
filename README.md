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
![image](https://user-images.githubusercontent.com/115543366/227861712-92a8cb5a-21d1-41b8-8dbb-b94c9328cfba.png)


4. Compute the y -intercept of the line by using the formula:  
![image](https://user-images.githubusercontent.com/115543366/227861889-34e5fca5-048c-4070-93a2-ff4762779a08.png)


5. Use the slope m and the y -intercept to form the equation of the line.  

6. Obtain the straight line equation Y=mX+b and plot the scatterplot.  

*/Program to implement univariate Linear Regression to fit a straight line using least squares.  
Developed by: M.Mano 
RegisterNumber: 212221040100 */  

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

Output:
Best fit line:  
![image](https://user-images.githubusercontent.com/115543366/227862462-2879586d-ef0c-41c9-8708-dc5e9a914873.png)


Finding Mean of x:  
![image](https://user-images.githubusercontent.com/115543366/227862419-45e74530-e46a-4d1c-b7f7-ffe1246c2b3e.png)


Finding the slope m:  
![image](https://user-images.githubusercontent.com/115543366/227862378-65062ec2-9966-49ae-93cb-61393a25e800.png)


Finding the y intercept:  
![image](https://user-images.githubusercontent.com/115543366/227862289-670eda87-6857-4b3d-a816-9725f4335615.png)


Equation of line:  
![image](https://user-images.githubusercontent.com/115543366/227862241-a2261c3e-8024-487f-9422-4d28876f9e76.png)


Finding Mean of y :  
![image](https://user-images.githubusercontent.com/115543366/227862171-568d5cbb-0def-4fea-a8cb-e3928e0781b8.png)


Result:  
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.  
