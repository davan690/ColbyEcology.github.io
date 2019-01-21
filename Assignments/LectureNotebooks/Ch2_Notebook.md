---
layout: assignment
title: "Chapter 2 notebook"
---

# Exercises based on Vandermeer and Goldberg
**Due 05 MARCHy**

### 2.1
Given the projection matrix:
$$\begin{bmatrix}
0 & 1 & 4 \\
0.7 & 0 & 0 \\
0 & 0.2 & 0
\end{bmatrix}$$
begin with 10 individuls in the first age class and project the population 15 times. Plot the total population over time. Verbally describe what patterns you may see in the data.

### 2.2
From the data in exercise 2.1, plot the logarithm (your favorite base) of the population density over time.

### 2.3
From the projection in exercise 2.1, plot the population densities of the age categories over time. Compare the pattern with the results of exercise 2.1.

### 2.4
Given the projection matrix
$$\begin{bmatrix}
0   & 3   & 8   & 1 \\
0.7 & 0   & 0   & 0 \\
0   & 0.3 & 0   & 0 \\
0   & 0   & 0.1 & 0
\end{bmatrix}$$
supopose the population is introduced onto an island with 10 of the oldest individuals. Project the population 20 times, and graph the total number over time.

### 2.5
Using the projection matrix in exercise 2.4, suppose the population is introduced onto an island with 10 of the third-oldest age category. Project the population 20 times, and graph the total number over time. Compare to the results of exercise 2.4.

### 2.6
Using the results from exercise 2.5, calculate the ratio of the number of individulas in age category 2 to those in category 1, and plot the ratio over time. Do the same for age categories 4 and 3. What do you notice?

### 2.7
Consider the following projection matrix representing a population with five age classes:
$$\begin{bmatrix}
0 & 5 & 3 & 2 & 1 \\
0.9 & 0 & 0 & 0 & 0 \\
0 & 0.3 & 0 & 0 &  \\
0 & 0 & 0.1 & 0 & 0 \\
0 & 0 & 0 & 0.05 & 0
\end{bmatrix}$$
Begin with a population distributed as 0, 0, 0, 0, 10 individuals respectively across age classes. Project the population 20 times units and plot the total number over time (it's probably easiest to plot density on a logrithmic scale).

### 2.8
Repeat exercise 2.7, but begin with 80, 16, 5, 1, and 1 individuals. Compare the results with the results from exercise 2.7.

### 2.9
Using the projection matrix from exercise 2.4, begin with a population vector of 674, 263, 47, 3 (the stable age distribution), and project the population 10 time units. Plot the natural log of the total population density against time. Then calculate the rate of natural increase from this graph.

### 2.10 (I did it for you)
Using the same projection matrix as in exercise 2.9, multiply the matrix by itsef 10 times. Recall that you estimated the intrinsic rate of natural increase as 0.5603 in exercise 2.9. Verify equation 8 by calculating the vector $\mathbf{N}_{t+1}$ from $\mathbf{P}^{10}\mathbf{N}_t$ and then from $\lambda ^10\mathbf{N}_t$, using the stable age distribution for $\mathbf{N}_t$ and then plotting the two calculations against one another. I have done it below:  
```
proj.mat.n <- proj.mat4%*%proj.mat4%*%proj.mat4%*%proj.mat4%*%proj.mat4%*%proj.mat4%*%proj.mat4%*%proj.mat4%*%proj.mat4%*%proj.mat4%*%N0_2.9
lambda.n <- exp(slope*10)*N0_2.9
plot(x = proj.mat.n, y = lambda.n, las = 1, xlab = "Density using (projection matrix)^n", ylab = "Density using lambda^n", cex = 2, pch = 16)
  lines(x = proj.mat.n, y = lambda.n)
```  
As proved in the book, $\mathbf{P}^n\mathbf{N}_t = \lambda ^n\mathbf{N}_t$. **Nothing to do here, but it's needed to evaluate eqn. 8 and for exercise 2.11.**

### 2.11
Repeat the exercise 2.10 for the population vector $$\Biggl[ \begin{smallmatrix}200 \\ 300 \\ 50 \\ 40\end{smallmatrix}\Biggr]$$, which of course is not the stable age distribution.

### 2.12
Given the projection matrix $$\Bigl[ \begin{smallmatrix}0 & m \\ p & 0\end{smallmatrix}\Bigr]$$, find the two eigenvalues analytically. (*Reference the penultimate equation before the exercise that gives the equation for a determinant of a 2-by-2 matrix.*)

### 2.13
Given the projection matrix $$\Bigl[ \begin{smallmatrix}0 & 0.3 \\ 0.9 & 0\end{smallmatrix}\Bigr]$$, compute the eigenvalues by hand, the same way you did for exercise 2.11 (solving for $\lambda$). Beginning with $N_1 = 21.5$ and $N_2 = 23.6$, project the final matrix forward 30 times, plot the log of the total number against time, and estimate the rate of population growth from a line drawn on the plot. (*Recall from the previous chapter what the exponential rate of incrase looks like after taking a natural log.*) Does the estimate of the finite rate of population increase correspond to the computation of the dominant eigenvalue?

### 2.14
Given the projection matrix $$\Biggl[ \begin{smallmatrix}0&3&8&1 \\ 0.7&0&0&0 \\ 0&0.3&0&0 \\ 0&0&0.1&0  \end{smallmatrix}\Biggr]$$, compute the eigenvalues. But, instead of doing it by hand, let's let our "computers" do the work for us. Use `eigen()` over your matrix. The first of the `$values` output is the dominant (also described as the largest in the book) eigenvalue, which is the finite rate of population increase! (Right?! I love computers!) Project the population starting with the population vector $$\Biggl[ \begin{smallmatrix}76 \\ 86 \\ 99 \\ 14  \end{smallmatrix}\Biggr]$$, and directly estimate the dominant eigenvalue.


### 2.15
In a population of insects we find that there are, at a particular point in time, 1000 larvae, 50 pupae, and 5 adults. We find that after another census one month later we are able to estimate the probability of survival of a larva (assuming it remains a larva) as 0.7, the probability that the larva will turn into a pupa as 0.2, the probability that a pupa will survive as 0.1, the probability that the pupa will turn into an adult as 0.4, and the probability that an adult will survive as 0.5. Furthermore, an average adult produces 100 eggs, 50% of which appear (within that month) as larvae while the rest die. Construct the population matrix that takes into account all of these probabilities, and project the population one time unit (remember that the time unit is one month).

> In markdown, here is how you create a vector:  
`$$\Biggl[ \begin{smallmatrix} x \\ y \\ z \end{smallmatrix}\Biggr]$$`  
That looks like this: $$\Biggl[ \begin{smallmatrix} x \\ y \\ z \end{smallmatrix}\Biggr]$$.

> In markdown, here is how you create a matrix:  
`$$\Biggl[ \begin{smallmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{smallmatrix}\Biggr]$$`.  
That looks like this: $$\Biggl[ \begin{smallmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{smallmatrix}\Biggr]$$.

### 2.16
Project the population of exercise 2.15 ten times, and graph the total population over time. What is the rate of population increase?

### 2.17
Plot the proportion of each state over time (in three different graphs).

### 2.18
In a population of plants, we categorized individuals as small seedlings, large seedlings, small saplings, large saplings, and adults. Presuming that the plants in each stage either move to the next stage or stay in their own category during population growth, write the state projection matrix in general terms. (That is, fill out a matrix with values that would be 0 and which would not.)

### 2.19
At another site this same population has slightly different growth patterns and the variability of its growth is very large, such that occasionall the small seedlings grow all the way to small saplings during a single time unit. Furthermore, because of the severe weather, occasionally a large sapling has its top damaged and actual reverts to the small sapling stage. Modify the matrix of exercise 2.18 to account for these probabilities.