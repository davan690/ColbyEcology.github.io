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




