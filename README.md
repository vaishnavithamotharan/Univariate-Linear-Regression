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
Program to develop to implement univariate Linear Regression to fit a straight line using least squares.

Developed by : SANTHI P Register no : 25016155
```
import numpy as np
import matplotlib.pyplot as plt
X= np.array([0,1,2,3,4,5,6,7,8,9])
Y= np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(X,Y)
plt.show()
X_Mean=np.mean(X)
Y_Mean=np.mean(Y)
num=0
den=0
for i in range(len(X)):
    num+=(X[i]-X_Mean)*(Y[i]-Y_Mean)
    den+=(X[i]-X_Mean)**2

m=num/den
b=Y_Mean-(m*X_Mean)
print(f"Slope : {m}\nIntercept : {b}")
Y_Pred=(m*X)+b
print(f"Predicted values are : \n{Y_Pred}")
plt.scatter(X,Y,color='Red')
plt.plot(X,Y_Pred,color='Blue')
plt.show()
```
## Output
<img width="863" height="740" alt="Screenshot 2025-12-24 210901" src="https://github.com/user-attachments/assets/1a3ca7b3-ae3e-4f7f-8227-b756dc8ea7b2" />
<img width="802" height="483" alt="Screenshot 2025-12-24 210929" src="https://github.com/user-attachments/assets/4387104b-7c4f-405d-9719-de616a59853f" />
<img width="938" height="297" alt="Screenshot 2025-12-24 210953" src="https://github.com/user-attachments/assets/156d0173-2452-428e-8f3c-975832f7d4ca" />
<img width="827" height="633" alt="Screenshot 2025-12-24 211034" src="https://github.com/user-attachments/assets/de130198-e8a1-4181-b9e4-7445f6728602" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
