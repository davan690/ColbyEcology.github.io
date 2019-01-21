---
title: "Chapter 8 notebook"
layout: assignment
---

# Exercises based on Vandermeer and Goldberg
**Due 23 April 2018**

For the lecture notebook this week, I ask that you analyze two two-species models of competition. The two models are the $K$ model and the $r-\alpha$ model:

$$\frac{dN_1}{dt} = r_1 N_1\left(\frac{K_1 - N_1 - \gamma _1N_2}{K_1}\right) \\
\frac{dN_2}{dt} = r_2 N_2\left(\frac{K_2 - N_2 - \gamma _2N_1}{K_2}\right)$$

and

$$\frac{dN_1}{dt} = r_1 N_1 - \alpha _{11}N_1^2 - \alpha {12} N_1N_2\\
\frac{dN_2}{dt} = r_2 N_2 - \alpha _{22}N_2^2 - \alpha {21} N_2N_1$$

For each model, I would like for you to analytically solve for the nullclines. Each of the two models should have 4 nullclines.

Next, I would like for you to plot the nullclines and vector field for four cases for each of the two models (8 cases in total). Two cases should include where the non-trivial (i.e., not $N_i^* =0$) nullclines (hereafter, nullclines) do not cross, resulting in one species competitively excludes the other. One case should include where the nullclines cross and both species coexist. The final case should be where the nullclines cross, but one species ultimately exclues the other (initial-condition dependency). The only parameters that you really need to change are the interacion terms: $\gamma _i$ in the $K$ model and $\alpha _{ij}$ in the $r-\alpha$ model.

For each graph, use the function `points()` to place a point for all 4 (or 5 if you put one at the trivial equilibrium, $(0,0)$) joint equilibira. Then, use the function `text()` to label the value of each point. There are only three arguments to place text on a plot, the x coordinate, the y coordinate, and the text. See `?text` to see the function's documentation.

Last, verbally elaborate on the the above. The intercepts are criteria that determine the outcome of the interaction—and incredibly important finding that will determine species coexistence or exclusion. Reference your text (and the competition slides) for assistance after you've attempted to think some of it through.