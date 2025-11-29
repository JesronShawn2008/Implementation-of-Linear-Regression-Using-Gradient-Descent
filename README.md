# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the dataset, extract the independent variable (R&D Spend) and dependent variable (Profit), then apply feature scaling to normalize the input values.

2. Initialize the model parameters (slope m and intercept c) and set the hyperparameters for gradient descent (learning rate and number of iterations).

3. Compute predictions using the current values of m and c, calculate the gradients for both parameters, and update them iteratively using gradient descent.

4. Compute and display the cost during initial iterations, then output the final slope, intercept, and predicted profit values for all samples.

## Program:
```
/*
Program to implement the linear regression using gradient descent.
import pandas as pd
import numpy as np

df = pd.read_csv("Startups.csv")

X = df["R&D Spend"].values.astype(float)
Y = df["Profit"].values.astype(float)

X = (X - X.mean()) / X.std()

m = 0 
c = 0  

alpha = 0.01
iterations = 1000

n = len(X)

for i in range(iterations):
    y_pred = m * X + c

    dm = (-2/n) * sum(X * (Y - y_pred))
    dc = (-2/n) * sum(Y - y_pred)

    m = m - alpha * dm
    c = c - alpha * dc

    if i <= n:
        cost = (1/n) * sum((Y - y_pred) ** 2)
        print(f"Iteration {i}, Cost={cost:.4f}, m={m:.4f}, c={c:.4f}")

print("\nFinal Slope (m):", m)
print("Final Intercept (c):", c)

final_predictions = m * X + c
print("\nPredicted Profits:\n", final_predictions)

Developed by: Jesron Shawn C J
RegisterNumber:  25012933
*/
```

## Output:
<img width="808" height="731" alt="image" src="https://github.com/user-attachments/assets/4c44c1c6-8826-4605-ab21-7c606d3916e4" />

<img width="904" height="312" alt="image" src="https://github.com/user-attachments/assets/e8b983b8-3453-49f9-b3d5-ddfabf101207" />



## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
