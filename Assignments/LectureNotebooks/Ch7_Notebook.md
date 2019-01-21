---
title: "Chapter 7 notebook"
layout: assignment
---

# Exercises based on Vandermeer and Goldberg
**Due 16 April 2018**

### 6G
Plot a time series, phase plane, and describe the 4 nullclines for a predator-prey model where prey grow exponentially, the predation rate follows a Type II functional response, and predators have a constant death rate (pgs. 164 and 165 from V&G). Use parameter values $r = 1.1$, $g = 1$, $c = 3$, and $m = 1$. Also, add a `trajectory()` curve, starting near the interior equilibrium. What happens?

### 6H
Plot 3 time series(es?), 3 phase planes, and describe the 4 nullclines for a predator-prey model where prey grow logistically, the predation rate follows a Type II functional response, and predators have a constant death rate (pg. 166 from V&G). Use parameter values $r = 1.5$, $K = 10$, $c = 1$, and $g = 3$. The parameter that I would like for you to vary across the three is $m$, which I would like you to set to 0.66, 0.5, and 0.45. Also add a `trajectory()` curve and make sure to start from the same densities for the three simulations.

Verbally describe the differences between the three.

### 7.4
The proportion of *Daphnia* infected duing a period of 15 days is, in sequence, 0.01, 0.03, 0.03, 0.1, 0.14, 0.3, 0.3, 0.58, 0.7, 0.7, 0.92, 0.92, 0.96, 0.97, 099, 0.99. Plot the time series.


### 7.7
Equation 1 is a perfectly fine representation of the accumualtion of infected individuals in the population. What equation would describe the rate of change in the number of susceptibles in the population? What would be the integrated form of that equation (think about 7.5 and single spiecies models)?


### 7.8
Begin with a very small infection ($I_0 = 0.001$) and use the integrated form of the mass action equation (7.5) to compute the time series for the susceptible (make a solid line) and infected (make a dashed line [in `plot()` or `lines()` use the argument `lty = 2`, which is abbr. for "line type"]) populations, with $\beta = 0.9$ (color the lines black), then with $\beta = 0.1$ (color the lines red). Plot susceptibles and infecteds on the same graph, but one graph for each $\beta$. (Use the same length of time over which you're plotting, and ensure that you capture the dynamics of each.)