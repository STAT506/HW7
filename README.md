# HW7


### Q1. (8 pts) 
Consider the binomial sampling distribution.  In classical inference, once you observe data (x), you might write down the 95\% confidence interval for p as

![wald eqn](https://latex.codecogs.com/gif.latex?%5Chat%7Bp%7D%20%5Cpm%201.96%20%5Csqrt%7B%5Cfrac%7B%5Chat%7Bp%7D%281-%5Chat%7Bp%7D%29%7D%7BN%7D%7D)

where ![phat](https://latex.codecogs.com/gif.latex?%5Chat%7Bp%7D%20%3D%5Cfrac%7Bx%7D%7BN%7D). This follows from the asymptotic normality assumption of the estimator.

Generate a uniform spacing of p's from .01 to .99, with a step size of .01. Under each value of p, generate a Binomial random number with N=10. Now construct the confidence interval specified above. Since you know the actual value of p, you can confirm if this interval does in fact cover the *true* parameter.

Repeat this 10,000 times for each value of p, and keep track of the frequency of times each of the 10,000 repetitions cover the known parameter. Show a plot of the behavior of the "true" coverage probabilities for the full range of p's (The y-axis will have frequency on it and the x-axis will be over p).

Repeat the exercise with N = {30,50,100}. Conclude with your thoughts on the experiment. Are you surprised?

### Q2. (8 pts)

Continue the process of testing coverage of the regression coefficients with contaminated error structures. In particular, simulate data for the regression model with the following parameters

```
n <- 100
x <- runif(n)
beta <- 1
sigma <- .1
```
and a residual term from the following four families.

```
library(gk)
rgh(num_sims,A = 0, B = 1, g = 0, h = 0)
rgh(num_sims,A = 0, B = 1, g = 0, h = .5)
rgh(num_sims,A = 0, B = 1, g = .5, h = 0)
rgh(num_sims,A = 0, B = 1, g = .5, h = .1)
```

Report your results.

### Q3. (2 pts)

How do you suppose the results for Q2 would change if n was 10 or 10,000?
