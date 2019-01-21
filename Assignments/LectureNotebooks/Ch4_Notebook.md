---
title: "Chapter 4 notebook"
output: html_document
layout: assignment
---

# Exercises based on Vandermeer and Goldberg
**Due 19 March 2018**

### 4.1
The integrated logistic equation is

$$N(t) = \frac{KN(0)}{(K - N(0))\exp(-rt) + N(0))}$$

Use this equation to generate a time series of $N$ versus $t$. Use parameters $r = 1.5$, $K = 100$


### 4.2
Repeat exercise 4.1 wth $ r= -0.1$, but use a time frame of 0 to 100. Describe what is happening.

### 4.3
Recall the population model of the Ricker equation from chapter 1

$$N_{t+1} = rN_t\exp(1 - bN_t)$$.

Let $r = 2.5$ and $b = 2.5$ and project the population 45 times units, beginning with an initial population size of 0.01. What is the pattern of the time series (don't forget this is a discrete-time equation)?

### 4.4 (skip)

### 4.5 (skip)

### 4.6
The exponential (density-independent differential equation) decribes the dynamics of a single population, which means that it is a dynamic system in one dimension. Its only equilibrium values is $N^* = 0$. Make two graphs of the deritative $\left(\frac{dN}{dt}\right)$ (vertical axis) as a function of $N$ (horizontal axis) for $r = 1.0$ and $r = 1.5$.

### 4.7
The logisitic equation also describes the dynamics of a single population but with two equilibrium points, $K$ and 0. Plot the derivative $\left(\frac{dN}{dt}\right)$ as a function of $N$ for $r = 1.0$, $K = 1.2$; $r = 1.5$, $K = 1.2$; and $r = 1.5$, $K = 1.8$.

### 4.8 (skip)

### 4.9
Assume that a population is growing according to the logistic equation. To make things simple, presume that the value of both $r$ and $K$ is 1.0 (i.e., we represent the population as varying between 0 and 1). The equilibrium value will be

$$0 = N - N^2$$,

which is a quadratic equation and has two roots, which are, by inspection, 0 and 1. Now suppose that a manager decides to impose a fixed harvesting rate on the popluation such that a constant number of individuals will be removed each year. A sensible model for this situation might be

$$\frac{dN}{dt} = N(1 - N) - N_F$$,

where $N_F$ is the fixed number (actually the proportion) of individuals removed. Plot the derivative versus $N$ for the following values of $N_F$: 0, 0.125, 0.25, and 0.5. Also, directly solve for the roots (using the quadrative formula; remember, $N_F$ is a constant). What do you conclude?

### 4.10
In chapter 1 (exercise 1.17) you used the logistic map to project the population 50 times with values of $\lambda = 1.5\text{, }2.0\text{, }3.0\text{, and }3.5$. Do the same for $\lambda = 3.4\text{, } 3.5\text{, } 3.56\text{, } 3.565\text{, and } 3.567$, starting with 0.8 individuals and projecting 100 time steps (include plots). Note that at the end of the run the numbers tend to repeat themselves in a regular sequence, For example, for $\lambda = 3.4$ the numbers go from 0.452 to 0.842 and then back again to 0.452, which is to say that there is a two-point cycle. How many points are in the cycles at the ends of the runs of the other values of $\lambda$? Plot the last 20 values of each trajectory (vertical axis) against the value of $\lambda$ *on the same graph*.

### 4.Extra
Now we wish to look to see how the cycling (or lack thereof) occurs over a greater range of $\lambda$. Create a sequence of $\lambda$s from 2.5 to 4 by one one-thousandth. Then, create a loop that numerically solves the logistic map for each value of $\lambda$ and ads points to a preexisting graph (change your pointsize using `cex = 0.25` [the default is 1.0] within `points()` and change your point types to solid using `pch = 16`). This will probably be your first bifurction diagram—revel in it after you're finished.
