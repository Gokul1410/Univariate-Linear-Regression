# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: GOKUL C
#register number: 212223240040

import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)


plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()

```
## Output

![Screenshot 2024-05-17 093351](https://github.com/Gokul1410/Univariate-Linear-Regression/assets/153058321/ac0a15d8-0497-4aa5-8e70-65ebc3894e32)

![216226396-d73caaf5-30d7-4ced-837c-03c056714da8](https://github.com/Gokul1410/Univariate-Linear-Regression/assets/153058321/a55d4fb3-51ef-4d12-8b93-af000e6ebd47)
![216226416-e476b56d-92b5-4ad1-8fcf-751adc00de30](https://github.com/Gokul1410/Univariate-Linear-Regression/assets/153058321/8c4c36b7-26be-4cca-b85a-784819054267)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
