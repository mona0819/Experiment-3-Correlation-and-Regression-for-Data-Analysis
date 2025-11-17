# Experiment-3-Correlation-and-Regression-for-Data-Analysis

# Aim: 
	To analyse given data using co-efficient of correlation and regression line 
  
  <img width="1180" height="120" alt="image" src="https://github.com/user-attachments/assets/62ba8618-34f6-4718-9233-b36f6ca975ff" />
  
# Software Required: Python 

# Theory
1. Correlation measures the strength and direction of the relationship between two variables (say, X and Y).
  
2. If one variable changes, correlation tells us how the other variable changes on average.
   
3. The correlation coefficient (r) ranges from –1 to +1: +1 means perfect positive correlation, –1 means perfect negative correlation, and 0 means no correlation.
   
4. Regression shows how one variable (Y) depends on another variable (X). It provides a line (equation) that best fits the data.
   
5. The regression line of Y on X is expressed as:  Y = a + bX,  where a is the intercept and b is the regression coefficient (slope).
   
# Algorithm 

<img width="1143" height="477" alt="image" src="https://github.com/user-attachments/assets/d3d41b8d-bee6-4b5f-a6fe-ef6997126cf2" />

# Program:
Name: Mohana Priya D
Reg no: 25016734
Slot name: 3P1-1
```
import numpy as np
import math
import matplotlib.pyplot as plt
x = [int(i) for i in input("Enter x values (space separated): ").split()]
y = [int(i) for i in input("Enter y values (space separated): ").split()]
if len(x) != len(y):
  raise SystemExit("Error: x and y must have the same number of values.")
N = len(x)
Sx = 0
Sy = 0
Sxy = 0
Sx2 = 0
Sy2 = 0
for i in range(N):
  Sx += x[i]
  Sy += y[i]
  Sxy += x[i] * y[i]
  Sx2 += x[i]**2
  Sy2 += y[i]**2
den = math.sqrt((N * Sx2 - Sx**2) * (N * Sy2 - Sy**2))
if den == 0:
  raise SystemExit("Denominator zero when computing correlation.")
r = (N * Sxy - Sx * Sy) / den
print("The Correlation coefficient is %0.3f" % r)
byx = (N * Sxy - Sx * Sy) / (N * Sx2 - Sx**2)
xmean = Sx / N
ymean = Sy / N
print("The Regression line Y on X is ::: y = %0.3f + %0.3f (x-%0.3f)" % (ymean, byx, 
xmean))
plt.scatter(x, y) 
def Reg(xv):
  return ymean + byx * (xv - xmean)
x_plot = np.linspace(min(x), max(x), 51)
y_plot = Reg(x_plot)
plt.plot(x_plot, y_plot, 'r')
plt.xlabel('x-data')
plt.ylabel('y-data')
plt.legend(['Regression Line', 'Data points'])
plt.grid(True)
plt.show()
```
https://colab.research.google.com/drive/1cg3jwmQeAM4HDvoR9lu1m6RVopc1mMlV?usp=sharing



# Output:
```
Enter x values (space separated): 25 28 35 32 31 36 29 38 34 32
Enter y values (space separated): 43 46 49 41 36 32 31 30 33 39
The Correlation coefficient is -0.394
The Regression line Y on X is ::: y = 38.000 + -0.664 (x-32.000)
<img width="727" height="551" alt="Screenshot (20)(1)(1)" src="https://github.com/user-attachments/assets/63171968-c541-452d-8393-9e6384dbb0a8" />
```



# Result
  The correlation and regression for data analysis of objects from feeder using probability distribution are calculated.




