# Multiplying Vectors

When multiplying a vector with a regular number, we just multiply every value in the vector with the regular number. So:

$$
\vec{a} = \begin{bmatrix}  2\\   1\end{bmatrix} 
$$

Is our vector and when we multiply it by 3 we get:

$$
3\vec{a} = 3 \begin{bmatrix}  2\\   1\end{bmatrix} =\begin{bmatrix}  2 \times 3\\   1 \times 3\end{bmatrix} = \begin{bmatrix}  6\\   3\end{bmatrix} 
$$

This is the first vector: $\vec{a}$

![image.png](Subject-Notes/Computing/Multiplying%20Vectors/image.png)

This is the vector after multiplying by 3:

![image.png](Subject-Notes/Computing/Multiplying%20Vectors/image%201.png)

So the direction has not changed but the magnitude has changed, it is now 3 times longer. Therefore, we can say that we have scaled this vector up by 3. This applies when also multiplying by a negative number, it will just change the direction to the opposite, like on a number line.

# Applying so far

Lets try this question now

$$
\vec{a}=\begin{bmatrix}  0\\   -1 \\ 2 \\ 3\end{bmatrix},\ \vec{b} = \begin{bmatrix}  4\\   -2 \\ 0 \\ 5\end{bmatrix}  \text{where } \vec{a}, \vec{b} \in \R^4 \\ 4\vec{a} - 2\vec{b} = ?
$$

Solution:

$$
4\begin{bmatrix}  0\\   -1 \\ 2 \\ 3\end{bmatrix} - 2 \begin{bmatrix}  4\\   -2 \\ 0 \\ 5\end{bmatrix} \\ \begin{bmatrix}  0\\   -4 \\ 8 \\ 12\end{bmatrix} -  \begin{bmatrix}  8\\   -4 \\ 0 \\ 10\end{bmatrix} \\ \begin{bmatrix}  -8\\   0 \\ 8 \\ 2\end{bmatrix} 
$$