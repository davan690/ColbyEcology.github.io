---
layout: assignment
title: "Chapter 2 Problem Notes"
---

# Chapter 2 Problem Notes

2.1. **Here is the ansnwer to 2.1.** To multiply the population sizes of multiple subpopulations (e.g., different ages, here) by their survival and reproduction, it would look like this:

```{r}
# Create the projection matrix, initial pop sizes, and test
   proj.mat <- matrix(data = c(0, 0.7, 0, 1, 0, 0.2, 4, 0, 0), nrow = 3, ncol = 3)
   N0 <- matrix(data = c(10, 0, 0), ncol = 1)
   proj.mat%*%N0 # see that it works once; also, use of matrix multiplier (inner product)

# Set simulation parameters
   n.steps <- 11
   vec.steps <- 1:n.steps
   N <- matrix(data = NA, nrow = length(N0), ncol = n.steps) # 11 to run 10 times after N0
   N[,1] <- N0

# Run loop
   for (i in 2:n.steps) {
      N[,i] <- proj.mat%*%N[,i-1]  
   }

# Function to sum columns to give total population size (dimension 2)
   totalN <- apply(X = N, MARGIN = 2, FUN = sum)

# Plot points at each step and connect them with a line
   plot(x = vec.steps, y = totalN, type = "l", las = 1, xlab = "Time step", ylab = "Total population")
   points(x = vec.steps, y = totalN, pch = 16, cex = 1.5)
```
Note that I use `matrix()` to create the population projection matrix and create another matrix that has one colum to represent the population at time $t$. Also, I created a $N$ matrix where we will save the data becuase we want to save each age class's population size (in the rows) at each time step (columns).  Hopefully this helps a bit.


2.2. For the first question, you can ignore what would be the best fit. But answer the second. To plot the last five steps, subset the matrix columns (e.g., pseudocode: `my.mat[, columns you want]`)

2.3. Use `lines()` to plot each row of the matrix (which corresponds to each age class).

2.4. None. It's structurally the same as 2.1.

2.5. None.

2.6. Ratio means divide, so you'd divide one age class over time over another age class over time.

2.7. None.

2.8. None.

2.9. None.

2.10. I've done this for you:

Using the same projection matrix as in exercise 2.9, multiply the matrix by itsef 10 times. Recall that you estimated the intrinsic rate of natural increase as 0.5603 in exercise 2.9. Verify equation 8 by calculating the vector $\mathbf{N}_{t+1}$ from $\mathbf{P}^{10}\mathbf{N}_t$ and then from $\lambda ^{10}\mathbf{N}_t$, using the stable age distribution for $\mathbf{N}_t$ and then plotting the two calculations against one another.

```{r}
proj.mat.n <- proj.mat4 %*% proj.mat4 %*% proj.mat4 %*% proj.mat4 %*% proj.mat4 %*% proj.mat4 %*% proj.mat4 %*% proj.mat4 %*% proj.mat4 %*% proj.mat4 %*% N0_2.9

lambda.n <- exp(slope*10)*N0_2.9
plot(x = proj.mat.n, y = lambda.n, las = 1, xlab = "Density using (projection matrix)^n", ylab = "Density using lambda^n", cex = 2, pch = 16)
  lines(x = proj.mat.n, y = lambda.n)
```

2.11. None.

2.12. Reference the antepenultimate (third-to-last) equation before the exercise that gives the equation for a determinant of a 2-by-2 matrix. Show steps.

2.13. None.

2.14. Let's let our "computers" compute the eigenvalues and do the work for us. Use `eigen()` over your matrix. The first of the `$values` output is the dominant (also described as the largest in the book) eigenvalue, which is the finite rate of population increase! (Right?! I love computers, too!) Still do the remainder of the problem, estimating the dominant eigenvalue, etc.

2.15. 
> In markdown, here is how you create a vector:  
`$$\Biggl[ \begin{smallmatrix} x \\ y \\ z \end{smallmatrix}\Biggr]$$`  
That looks like this: $$\Biggl[ \begin{smallmatrix} x \\ y \\ z \end{smallmatrix}\Biggr]$$.

> In markdown, here is how you create a matrix:  
`$$\Biggl[ \begin{smallmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{smallmatrix}\Biggr]$$`.  
That looks like this: $$\Biggl[ \begin{smallmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{smallmatrix}\Biggr]$$.

2.16. None.

2.17. None.

2.18. Write in the matrix elements any way you see fit. Convention is a subscript for the row and column; e.g., the probability that the second-year olds have come from the first-year olds could be written as $p_{21}$ in the third row and second column (assuming we have an age class "$0$")).

2.19. None.