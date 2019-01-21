---
layout: assignment
title: "Chapter 1 notebook"
---

# Exercises based on Vandermeer and Goldberg
## For the draft due 16 Feb., modified Exercises 1.1–1.8

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

## For the full notebook due 26 Feb, all exercises (1.1–1.18) (to appear week 01)

# Additional problems