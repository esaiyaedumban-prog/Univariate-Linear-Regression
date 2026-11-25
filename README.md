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
# DEVELOPED BY : ESAIYA E
# REFERENCE NUMBER : 26014140


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
</br>

<img width="1920" height="1080" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/d7ca74e5-97d9-4164-88d1-241e0306ae08" />
<img width="1920" height="1080" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/1487a7a9-4d47-46f1-8c3f-4f9d8997db49" />
<img width="1920" height="1080" alt="Screenshot (32)" src="https://github.com/user-attachments/assets/625b0dc6-0419-40e6-b2e9-9c7ee9b06294" />


</br>
</br>
</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
