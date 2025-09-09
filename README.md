# Programming Assignment 2

This repository contains a Jupyter Notebook (`PA2.ipynb`) that demonstrates two programming exercises using the **NumPy** library.

## Exercise 1: Normalization

This section of the notebook shows how to perform **Z-score normalization** on a randomly generated 5x5 NumPy array.

The process involves these steps:
1.  A 5x5 array `x` is created with random values.
2.  The mean (`mean`) and standard deviation (`sd`) of the array are calculated.
3.  Each element in the array is normalized using the formula `z = (x - mean) / sd`.
4.  The normalized array is then saved to a file named `X_normalized.npy`.

## Exercise 2: Divisible by 3

This section demonstrates how to manipulate and filter a 10x10 NumPy array.

The key steps are:
1.  A 10x10 array `x_1` is created, containing the integers from 1 to 100.
2.  A second array `x_2` is created by squaring each element of `x_1`.
3.  Elements from `x_1` that are divisible by 3 are filtered and stored in a new array, `orig_by_3`.
4.  Elements from `x_2` that are divisible by 3 are filtered and stored in a new array, `squared_by_3`.
5.  Finally, the arrays `orig_by_3` and `squared_by_3` are saved together in a single file named `div_by_3.npy`.

## How to Run

To run the notebook, you need to have **Python** and **Jupyter Notebook** installed.

1.  Clone this repository or download the `PA2.ipynb` file.
2.  Start the Jupyter Notebook server:
    ```bash
    jupyter notebook
    ```
3.  Your web browser will open, upload `PA2.ipynb`, and then click on `PA2.ipynb` to open and run the notebook.
