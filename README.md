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
Developed by: SHRAVANI M
RegisterNumber: 212224230263 
*/
```

#import the libraries

```
import numpy as np
import matplotlib.pyplot as plt

```
#input data

```
x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])
```
#Compute the means 

```
x_mean = np.mean(x)
y_mean = np.mean(y)
```
#Calculate numerator and denominator for the slope
```
num = 0
denom = 0
for i in range(len(x)):
    num += (x[i] - x_mean) * (y[i] - y_mean)
    denom += (x[i] - x_mean)**2

```
#Compute slope and intercept 

```
m = num / denom
b = y_mean - m * x_mean

```
predict y values
```
y_predicted = m * x + b
print(y_predicted)
```
#Display results 
```
print(m, b)
```
# plot the results
```
plt.scatter(x, y)                # Plot the actual data points
plt.plot(x, y_predicted, color='red')  # Plot the regression line
plt.show()

```
## Output:
#predict y values 

<img width="423" height="107" alt="image" src="https://github.com/user-attachments/assets/4c4b7ea4-d2b3-4c77-a56f-1a2924c1943d" />


#Display results

<img width="332" height="67" alt="image" src="https://github.com/user-attachments/assets/ad8e1372-3e54-4c71-944e-3f4742c2f264" />

#Plot 

<img width="697" height="508" alt="image" src="https://github.com/user-attachments/assets/ddcce2e1-1cb3-4697-8e34-a68f69371833" />


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
