---
layout: post
bigtitle:  "Writing Math Formulas in Python (Linear Algebra)"
subtitle:   "python"
categories:
    - study
tags:
  - etc
comments: true
published: true
---

# Writing Math Formulas in Python

In machine learning projects, I sometimes run into a situation where I have to write math formulas.

I created this for my reference but wanted to share with you all how to write basic math formulas in python.


## Indexing

$$x_i$$

is the $$i^{th}$$ value/element of a vector x.

~~~python
x = [10, 20, 30]
i = 0
print(x[i]) # = 10

for i in range(len(x)):
  print(x[i])
~~~
This can be represented in a 2D vectors.
$$x_{ij}$$

~~~python
x = [ [10, 20, 30], [40, 50, 60] ]
i = 0
j = 0
print(x[i][j])  # = 10

for i in range(len(x)):
  for j in range(len(x[i])):
    print(x[i][j])
~~~

## Sigma  

$$\sum^N_{i=1}x_i$$  

This formula represents the sum of all elements of a vector within a certain range
from lower limit $$i=1$$ to upper limit $$N$$
In python, it same as iterating from index 0 to index N-1

~~~python
x = [1, 2, 3, 4, 5]
result = 0
N = len(x)
for i in range(N):
  result += x[i]  # result = result + x[i]
print(result) # = 15
~~~

We can represent the code above by using built in functions as follows:

~~~python
x = [1, 2, 3, 4, 5]
result = sum(x)
~~~

## Average

$$\frac{1}{N}\sum^N_{i=1}x_i$$

Here, we calculate the average by dividing the Sigma we saw above by the number of elements in the vector.

~~~python
x = [1, 2, 3, 4, 5]
result = 0
N = len(x)
for i in range(N):
  result = result + x[i]
average = result / N
print(average)
~~~

which can be simlified as:

~~~python
x = [1, 2, 3, 4, 5]
result = sum(x) / len(x)
~~~

## PI

$$\Pi^N_{i=1}x_i$$

The next formula represents the product of all elements of a vecotor within a range.

~~~python
x = [1, 2, 3, 4, 5]
result = 1
N = len(x)
for i in range(N):
  result *= x[i]  # result = result * x[i]
print(result)
~~~

## Absolute Value

$$\Vert x\Vert$$  
$$\Vert y\Vert$$

The next formula indicates the absolute value.

~~~python
x = 10
y = -20
abs(x)  # 10
abs(y)  # 20
~~~

## Norm of vector

$$\Vert x\Vert$$  

Norm is used to calculate the size of a vector.
In python, it's the sum of the square of every element and taking a square root of it.


~~~python
import math

x = [1, 2, 3]
math.sqrt(x[0]**2 + x[1]**2 + x[2]**2)
# or
math.sqrt(sum([v**2 for v in x]))
~~~

## Function

$$f: X \rightarrow Y$$  

Function takes a domain of X and map it to Y.
In python, it calls the values of X and computes the values of Y.  

~~~python
def f(X):
  Y = ...
  return Y
~~~

$$f:R \rightarrow R$$  

R indicates that the input and the output are real numbers which can be any of the following: integer, float, irrational, rational.
In python, it any values excluding the complex numbers.

~~~python
import math
x = 1
y = 2.5
z = math.pi

def f(k):
  k = ...
  return k
~~~

$$f:R^d \rightarrow R$$

$R^d$ is a d-dimensional vector of a real number.
If d = 2, we would take a 2-D list and return the sum of the elements by using a function in python.
This represent mapping $R^d$ to $R$.

~~~python
X = [1,2]
f = sum
Y = f(X)
~~~

## Tensor

### Transpose

$$X^T$$

This changes the rows and columns of a matrix.
In python:

~~~python
import numpy as np
X = [[1, 2, 3],
    [4, 5, 6]]
np.transpose(X)
~~~
~~~
[[1,4],
 [2,5],
 [3,6]]
~~~

### Element wise multiplication  

$$z = x \odot y$$

This represents the multiplication of elements of two tensors.
In python, we multiply the elements of the two lists.  

~~~python  
import numpy as np
x = [[1,2],
    [3,4]]
y = [[2,2],
    [2,2]]
z = np.multiply(x,y)
~~~
Output:
~~~
[[2 4]
 [6 8]]
~~~

### Dot Product

$$xy$$  
$$x \cdot y$$

This is an inner product (aka dot product).
The two vectors should have the same dimension.

$$x = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix}, y = \begin{bmatrix} 4 \\ 5 \\ 6 \end{bmatrix}$$  

$$x^Ty = [1 \; 2 \; 3] \begin{bmatrix} 4 \\ 5 \\ 6 \end{bmatrix} = 1 \cdot 4 + 2 \cdot 5 + 3 \cdot 6 = 32$$

~~~python
x = [1, 2, 3]
y = [4, 5, 6]
dot = sum([i*j for i, j in zip(x, y)])
# 1*4 + 2*5 + 3*6
# 32
~~~

## Exclamation

$$x!$$

Factorial is a product of 1 through the number.
In python:

~~~python
x = 5
fact = 1
for i in range(x, 0, -1):
    fact *= i # fact = fact * i
print(fact)
~~~
There's a built-in function for this as well.

~~~python
import math
x = 5
math.factorial(x)
~~~
Output:  
~~~
# 5*4*3*2*1
120
~~~
