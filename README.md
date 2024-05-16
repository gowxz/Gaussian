## EX:6.Gaussian Elimination
## Date:
## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import numpy as np
2. Initialize array with zero 
3. Read the input matrix
4. Use back substitution method to find the value of variables
5. Print the output 

## Program:
```
Program to find the solution of a matrix using Gaussian Elimination.
Developed by:GOWTHAM S
RegisterNumber: 2305002008
```
```
 import numpy as np
 import sys 
n = int(input())
 a = np.zeros((n,n+1))
 x = np.zeros(n)
 for i in range(n):
    for j in range(n+1):
        a[i][j] = float(input())
 for i in  range(n):
        for j in range(i+1,n):
            ratio = a[j][i]/a[i][i]
            for k in range(n+1):
                a[j][k] = a[j][k] - ratio * a[i][k]
 x[n-1] = a[n-1][n]/a[n-1][n-1]
 for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]= x[i]/a[i][i]
 for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end =' ')
```

## Output:
![IMG-20240513-WA0009](https://github.com/gowxz/Gaussian/assets/155504997/efcd6de6-f8c9-423a-94f6-20391696a2ef)
![IMG-20240513-WA0008](https://github.com/gowxz/Gaussian/assets/155504997/6e8838b6-190b-4e8f-9323-8a1c38288c8f)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

