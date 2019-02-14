---
layout: assignment
title: "Chapter 1 Clarifications"
---

# Chapter 1 Problem Notes

1.1. Calculate by hand—say 5—enter manually (e.g., using `c()`) and plot in R.

1.2. Use function `segments()` to draw a line from the first to the last point. The arguments are: `x0 =`, `y0 =`, `x1 =`, and `y1 =`. The argumetns with 0s assign the x and y coordinates of the beginning of the line; the 1s, the end.

1.3. Do this by hand, but show a step or 2. To write math in R Markdown, use dollarsigns. For example,
`$1^2 + x = 5$`, or
`$\frac{1}{2} / N_{t - 1} > \log 4$`
will produce
$1^2 + x = 5$, and
$\frac{1}{2} \times N_{t - 1} > \log (4)$, respectively.

1.4. None.

1.5. Show a step or 2 in R.

1.6. Use the equation: $N(t) = N(0)\exp (rt)$ (equation 10 in the next section), for $t = 1–10$ in R. Make $t$ a sequence with small steps (say, 0.01).

1.7. If you have have a vector and you want to subtract an element from the follow element (e.g., the next time step from a previous one), that means you want to subract the first from the 2nd, the 2nd from the 3rd, etc. The hint with working with vectors is that you do all of these operactions if the vectors are the same length. E.g., `c(4, 5, 6) + c(7, 8, 9)` = `c(11, 13, 15)`. So, **if you were to take the second element to the last and subtract from those the first to the penultimate element, you'd find what what they are calling a "derivative."**.

Additionally, when you go to plot it, your derivative vector will be one shorter than the time step. This means you need to remove one element, so I'd suggest removing the last one. So, if your time step verctor was called `timestep`, if you use `deriv.timestep <- timestep[-length(timestep)]`, you will write a new vector after removing the last one. (If you subset and use a minus in front of a number, it will exclude it; `length()` returns the number of elements in a vector.)

1.9. Here, I've entered and generated the data for you:
```r
pop <- c(3278, 3347, 3417, 3486, 3558, 3632, 3708, 3785, 3861, 3936, 4011, 4084, 4156, 4226, 4298, 4372, 4447, 4522, 4601, 4682, 4762, 4844, 4927, 5013, 5099, 5185, 5273, 5357, 5440, 5521, 5601, 5681, 5762, 5840, 5918, 5995, 6072, 6147, 6222, 6297, 6373, 6449)

years <- seq(from = 1964, to = 2005, by = 1)
```

1.10. Eyeballing or fitting a line is fine.

1.11. None.

1.12. None.

1.13. Find the derivative of the logistic equation (eq. 17) with respect to $N$. I.e.,

$$\frac{{d}}{{{d}N}}\left(\frac{{dN}}{dt}\right) = rN\left(\frac{K - N}{K}\right)$$

1.14. Skip.

1.15. Skip.

1.16. By "exponential map," the authors mean "logistic map." Use a loop through your 50 time steps. Place all values of $\lambda$ on the same graph by using the function `lines(x = , y = )`.

1.17. None.

1.18. **No spreadsheet!!!** :) Simply plot the three models with the three parameters listed.