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
import numpy as np
import matplotlib.pyplot as plt

#Preprocessing Input data

x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(x,y)
plt.show()
#Building the model
x_mean=np.mean(x)
y_mean=np.mean(y)

num=0
den=0
for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    den+=(x[i]-x_mean)**2
m=num/den
c=y_mean-m*x_mean
print(m,c)
#Making predicitions
y_pred=m*x+c
print(y_pred)

plt.scatter(x,y) #actual
#plt.scatter(x,y_pred,color='red')
plt.plot([min(x),max(x)],[min(y_pred),max(y_pred)],color='red') #predicted
plt.show()

```
## Output
<img width="1046" height="823" alt="{6E6EE6DA-9E7F-4290-9FC7-8AB18F5099DE}" src="https://github.com/user-attachments/assets/1e5c1e9e-431a-4aff-bb4f-589cedf347b2" />
<img width="1045" height="641" alt="{733A072B-A5F4-4E8B-91E2-C4FB220DA20B}" src="https://github.com/user-attachments/assets/08d1fcf3-4512-40b7-9cf6-e04d0fbdc525" />
<img width="1044" height="694" alt="{44200750-BB7A-4885-948B-17D53627E943}" src="https://github.com/user-attachments/assets/02090507-8499-4ee2-a725-960e261f3aea" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
