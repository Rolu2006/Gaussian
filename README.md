# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
### Step 1:
numpy (np): Provides the zeros() function to create arrays/matrices.

sys: Provides sys.exit() to terminate the program in case of mathematical errors (like division by zero).


### Step 2:
input(): Reads user input as a string.

int(): Converts string input to an integer (number of equations and unknowns).


### Step 3:
np.zeros((rows, columns)): Creates a matrix or vector filled with zeros.
Nested loops to fill each row i and column j of matrix a.

float(input()): Reads user input, converts it to a float, and stores it in matrix a.
### Step 4:
Checks if diagonal element a[i][i] is zero (division not allowed).

sys.exit(): Terminates the program if division by zero would occur.
For each equation from bottom to top:

Start with the RHS.

Subtract all known values multiplied by their coefficients.

Divide by the coefficient of the unknown.

### Step 5:
Prints each value of x[i] to 2 decimal places.

%0.2f is format specifier to show two decimal places.

end='' avoids a new line between outputs.

## Program:
```
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f '%(i,x[i]),end='')
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: somalaraju rohini
RegisterNumber: rohini
*/
```

## Output:
![gaussian elimination]()






![Screenshot 2025-04-27 143806](https://github.com/user-attachments/assets/18486dfe-a1a1-4a1f-86dd-aa74b2ef7e66)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

