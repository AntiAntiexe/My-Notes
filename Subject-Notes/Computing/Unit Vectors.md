# Unit Vectors

# What we have already been doing

We have already seen that we can represent a vector with an arrow where the length is the magnitude and the direction is the direction of the vector. To represent this mathematically, starting from the tail of at the vector how far away is the head of the vector in the horizontal direction and how far away the head is in vertical direction.

![image.png](Subject-Notes/Computing/Unit%20Vectors/image.png)

So we can then represent this vector as an ordered list or a 2-tuple:

$$
\vec{v} = \begin{bmatrix}  2\\   3\end{bmatrix}
$$

# What are Unit Vectors

When in two dimensions we define our unit vectors in each of the dimensions that we are working in. So lets show the unit vectors for a 2 dimensional space:

$$
\hat{i} = \begin{bmatrix}  1\\   0\end{bmatrix} \\ \hat{j} = \begin{bmatrix}  0\\   1\end{bmatrix} 
$$

![image.png](Subject-Notes/Computing/Unit%20Vectors/image%201.png)

The i hat only goes one unit in the horizontal direction and no units to the vertical direction. J hat will only go in the vertical direction and no units in the horizontal direction. With these new vectors we can write any vector as a sum of scaled up versions of i hat and j hat

$$
\vec{v} = 2\hat{i} + 3\hat{j}
$$

You can notice that the scalars in the unit vector notation are he same horizontal and vertical values in the vector tuple notation $\begin{bmatrix}  2\\   3\end{bmatrix}$.

## Example

Given 

$$
\vec{v} = 2\hat{i} + 3\hat{j} \text{ and } \vec{b} = -1\hat{i} + 4\hat{j} \text{ what is } \vec{v} + \vec{b}
$$

$$
2\hat{i} + 3\hat{j} +(-1\hat{i} + 4\hat{j}) \\ = \hat{i} + 7\hat{j}
$$