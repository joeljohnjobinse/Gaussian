# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import sys and numpy modules
2. Take the order of the matrix as first input
3. Create the matrix with values as user input
4. Do the elimination
5. Print X0, X1 and X2 values

## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Joel John Jobinse
RegisterNumber: 23008174
'''
import sys
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    if matrix[i][j]==0.0:
        sys.exit("Divide by zero error")
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f"%(i,x[i]),end=' ')
*/
```

## Output:
![maths-exp6](https://github.com/joeljohnjobinse/Gaussian/assets/138955488/dbbcb99e-2c57-48aa-ae59-df2e536dc947)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

