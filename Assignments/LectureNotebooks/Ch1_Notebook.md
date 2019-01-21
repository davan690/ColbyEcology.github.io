---
layout: assignment
title: "Chapter 1 notebook"
---

# Exercises based on Vandermeer and Goldberg
**Due 26 February**

### 1.1
By hand, compute the expected number of individuals over time in a population with a single initial individual that grows according to equation 3 for $\lambda = 1.9$, $\lambda = 2.0$, and $\lambda = 2.1$, where $\lambda$ is the finite rate of increase. Enter your data in R using `c()` for 10 timesteps. For example: `lambda_1.9 <- c(1, 1.9)` (but with nine more entries). Plot the data as points and use the function `points()` to present all three trajectories on a single plot. Plot your data as a timeseries, meaning the horizontal axis is time (or timesteps, in this instance).

### 1.2
Plot the numbers aclculated in exercise 1.1 as ln($N$) versus time. Do this by creating a new object that is the natural log of the data from exercise 1.1. Plot all three growth curves again using the function `points()`. Calculate and report the equations of the three curves (lines are technically a type of curve, should that be what your data show). To write out math, just put dollar signs around your text: `$\lambda = 1.9$` (looks like $\lambda = 1.9$).

### 1.3
Derive an equation for doubling time in an exponentially growing population, and derive one for tripling time.

### 1.4
Plot the values computed in exercise 1.1 on a graph of $N_{t+1}$ on the vertical axis and $N_t$ on the horizontal axis for each value of $\lambda$ on a single graph. This time plot them as lines using the function `lines()` after `points()`.

### 1.5
The human population on a small island nation is said to be doubling every 20 years. What would be the value of $r$ (assuming an exponential model)?

### 1.6
Using the differential form (i.e., continuous time), suppose that $r = 0.5$. Compute $N$ as a function of $t$, again beginning with a single individual. Do the same for $r = 1.5$ and for $r = 1$. Graph all of the results.

### 1.7
Plot the derivative (which you can approximate by subtracting the current $N$ from its successive on and dividing by the change in time) as a function of $N$ for the data calculated in exercise 1.6 (use a small time interval, e.g., 0.01).

### 1.8
From the data calculated in exercise 1.7, divide the estimated derivative by the average number of individuals during the time period, and plot them over time. What is the result, and what does it mean?

### 1.9
For the UN data on the global human population, plot the time series. Next, plot how much the population changes (vertical axis) for a given density. Then plot the per-capita change against density. Describe, to the best of your abilities, the relationship and speculate on the type of function that would best *describe* these data.

### 1.10 
Graphically estimate the point at which the population population will stop growing (the number of individuals in the word at the point at which the observed trend will reach 0). How would various sections of the data, if considered alone, change your conclusions?

### 1.11
Using the UN data on the human population. What would be the value of the per-capita growth rate at $N = 0$? Consider and speculate on the meaning of this value.

### 1.12
Beginning with the exponential equation, assume that the rate of change decreases linearly with population density. Substitute $a - bN$ for $r$, and interpret $a$ and $b$ as they relate to 1.11.

### 1.13
Assuming that a population grows according to the logistic equation, what is the value of the population density that will give the maximum growth rate?

### 1.14 (Skip)

### 1.15 (Skip)

### 1.16
Using the logistic map and starting with 0.1 individuals, project the population 50 times with values of $\lambda =$ 0.1, 1.5, 2.0, 3.0, and 3.5. How does the time series change as a function of $\lambda$?

### 1.17
In exercise 1.4, successive values of population density were plotted against one another (i.e., $N_{t+1}$ was plotted against $N_t$). Repeat that exercise for $\lambda =$ 1.5, 2.0, 3.0, and 3.5, and then modify the equation to be the logistic map (eqn. 27) and make the graphs again for $\lambda =$ 1.5, 2.0, 3.0, and 3.5.

### 1.18
Plot $N_{t+1}$ against $N_t$ for the Beverton and Holt model, the Hassell model, and the Ricker model (eqns. 28–30), and compare them. Let $\lambda = 1$, $\alpha = 1$, and $b = 2$. If you wanted explore how the parameter values affect various aspects of the plot, verbally describe what you would do.


# Additional problems
None this week.