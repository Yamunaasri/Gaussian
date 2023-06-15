# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the numpy module to use the built-in functions for calculation.
2. Import the sys module to use the built-in functions.
3. Get input from the user for number of rows and add it by 1 for number of columns.
4. Using np.zeros() set the matrix as null matrix.
5. Using for loop get input from the user for each element in the matrix.
6. Using for loop we can perform the elementary row operations and find the final
matrix.
7. Print the values by solving the matrix using for loop with 2 point precision.
8. End the program.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: T S Yamunaasri
RegisterNumber: 212222240117

import numpy as np
import sys
#Reading number of unknowns
n=int(input())
#making numpy array of n x n+1 size and initializing
#To zero for storing augmented matrix
a=np.zeros((n,n+1))
#making numpy array of n size and initializing
#To zero for storing soultion vector
x=np.zeros(n)
#reading augmented matrix coefficient
for i in range(n):
for j in range(n+1):
a[i][j]=float(input())
#Applying gauss elemination
for i in range(n):
for j in range(i+1,n):
ratio=a[j][i]/a[i][i]
for k in range(n+1):
a[j][k]=a[j][k]-ratio*a[i][k]
#Back substitution
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
x[i]=a[i][n]
for j in range(i+1,n):
x[i]=x[i]-a[i][j]*x[j]
x[i]=x[i]/a[i][i]
#Displaying solution
for i in range(n):
print('X%d = %.2f'%(i,x[i]),end=' ')
*/
```

## Output:

![image](https://github.com/Yamunaasri/Gaussian/assets/115707860/9f4ed625-dc50-451d-a70a-625bfe5dde7c)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

