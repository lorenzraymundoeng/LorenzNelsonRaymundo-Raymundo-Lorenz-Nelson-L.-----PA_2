# Programming Assignment 2 | Raymundo, Lorenz Nelson L.
#### This is my submission for PA2 (Experiment 2 | Numerical Python)
This repository contains a Jupyter Notebook (`PA2.ipynb`) that demonstrates two programming exercises using the **NumPy** library.

Before we proceed, remember to import the numpy library to your notebook. This is a very important step because it will let you access all NumPy functions.
```Python
import numpy as np
```
#### Part 1: Normalization

The first exercise in this programming assignment (PA) shows how to perform **Z-score normalization** on a randomly generated 5x5 NumPy array.
\nTo do this, we must first create a 5x5 array.
```Python
x = np.random.random([5,5])
```
Now, knowing that the formula for Z-score normalization is ** (X-μ)/σ ** where μ is the mean and σ is the standard deviation.
To get the mean and the standard deviation, we can use a numpy function .mean() and .std()
```Python
mean = x.mean()
sd = x.std()
```
To get the Z-score normalization, we use the formula ** (X-μ)/σ **. Since μ is mean and σ is sd,
```Python
norm_x = (x-mean)/sd

# to display,
print(norm_x)
```
Lastly, according to the instructions, we must save this Normalized array as `X_normalized.npy`
To do this, we type in 
```Python
np.save('X_normalized.npy, norm_x)

# for displaying purposes,
print("\n\n Normalized ndarray saved to 'X_normalized.npy'")
```

## Exercise 2: Divisible by 3

This section demonstrates how to manipulate and filter a 10x10 NumPy array.

The key steps are:
1.  A 10x10 array `x_1` is created, containing the integers from 1 to 100.
2.  A second array `x_2` is created by squaring each element of `x_1`.
3.  Elements from `x_1` that are divisible by 3 are filtered and stored in a new array, `orig_by_3`.
4.  Elements from `x_2` that are divisible by 3 are filtered and stored in a new array, `squared_by_3`.
5.  Finally, the arrays `orig_by_3` and `squared_by_3` are saved together in a single file named `div_by_3.npy`.

## How to Run

To run the notebook, you need to have **Anaconda Navigator** installed and open **Jupyter Notebook**.

1.  Download the `PA2.ipynb` file.
2.  Start the Jupyter Notebook server:
    ```bash
    jupyter notebook
    ```
3.  Your web browser will open, upload `PA2.ipynb`, and then click on `PA2.ipynb` to open and run the notebook.
