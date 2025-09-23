# Programming Assignment 2 | Raymundo, Lorenz Nelson L.
#### This is my submission for PA2 (Experiment 2 | Numerical Python)
This repository contains a Jupyter Notebook (`PA2.ipynb`) that demonstrates two programming exercises using the **NumPy** library.

Before we proceed, remember to import the numpy library to your notebook. This is a very important step because it will let you access all NumPy functions.
```Python
import numpy as np
```
#### Part 1: Normalization

The first exercise in this programming assignment shows how to perform **Z-score normalization** on a randomly generated 5x5 NumPy array.\
To do this, we must first create a 5x5 array.
```Python
x = np.random.random([5,5])
```
Now, knowing that the formula for Z-score normalization is ** (X-μ)/σ ** where μ is the mean and σ is the standard deviation.\
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
Lastly, we must save this Normalized array as `X_normalized.npy`\
To do this, we type in 
```Python
np.save('X_normalized.npy, norm_x)

# for viewing purposes,
print("\n\n Normalized ndarray saved to 'X_normalized.npy'")
```

#### Part 2: Divisible by 3

The second exercise in this programming assignment demonstrates how to manipulate and filter a 10x10 NumPy array.\
We know that a 10x10 array must contain 100 elements. To do this, we use the .arange() function to create an evenly spaced array.
```Python
# With 1 (inclusive) and 101 (exclusive), this is an array that will contain values 1 to 100.
x = np.arange(1,101)
# Since this is still not arranged as a 10x10 array, we use the .reshape() function
x_1 = x.reshape(10,10)

# For viewing purposes,
print("Original Array:\n" , x_1)
```
According to the instructions, we need to create a 10x10 array of the SQUARES of the first 100 positive integers, and then find out which values are divisible by 3. \
To do this we must first square all the values inside array x_1,
```Python
x_2 = x_1**2 #This squares all of the values inside array x_1

#For viewing purposes,
print(\n Array with squared values:\n" , x_2)
```
Before finding all of the squared values that are divisible by three, it would be fun to also know which of the original values are divisible by 3.\
To do this, 
```Python
orig_by_3 = x[x % 3 == 0] # Modulo returns the remainder of a number when divided by a certain number x (in this case, 3). If the remainder is zero, then it means that the number is divisible by 3.
x_3 = orig_by_3.reshape(3,11) # This step is not necessary. But, knowing that from 1 to 100, there are 33 numbers that are divisible by 3. We can reshape the array to a 3x11 array to make it look more presentable

# For viewing purposes,
print("\n Original elements divisible by 3:\n" , x_3)
```

Similarly, we can use the same code to find the squared values that are divisible by 3. But of course, we must change x to x_2.
```Python
squared_by_3 = x[x_2 % 3 == 0] # Modulo returns the remainder of a number when divided by a certain number x (in this case, 3). If the remainder is zero, then it means that the number is divisible by 3.
x_4 = squared_by_3.reshape(3,11) # This step is not necessary. But, knowing that from 1 to 100, there are 33 numbers that are divisible by 3, then, there should still be 33 numbers that are divisible by 3 when squared

# To display,
print("\n Squared elements divisible by 3:\n" , x_4)
```
Lastly, we must save the elements divisible by 3 to `div_by_3.npy`\
To do this,
```Python
np.save('div_by_3.npy', x_3, x_4)

# For viewing purposes,
print("\n\n Elements divisible by 3 saved to 'div_by_3.npy'")
```

#### Pre-requisites
- Python 3.0 or later

#### Installation
These codes were created on Jupyter Notebook. Make sure to install Anaconda Navigator and access Jupyter Notebook. It's all for free! Alternatively, you could use VS Code to run the code.

#### How to Run
1.  Download the `PA2.ipynb` file.
2.  Start the Jupyter Notebook server:
3.  Your web browser will open, upload `PA2.ipynb`, and then click on `PA2.ipynb` to open and run the notebook.
