**1. Describe the null hypotheses to which the p-values given in Table 3.4
correspond. Explain what conclusions you can draw based on these
p-values. Your explanation should be phrased in terms of `sales`, `TV`,
`radio`, and `newspaper`, rather than in terms of the coefficients of the
linear model.**

The null hypotheses stats that there's no relationship between `Sales` and
`TV`, `radio` and `newspaper`; i.e. that these predictors have no relationship
with `Sales`. Because the p-values for both `TV` and `radio` are strongly
significant (virtually, 0), the null hypothesis can be rejected as there is
a really small possibility (<0.01%) that it's correct. On the other hand,
it's not statistically significant for `newspaper` as it's 0.86, showing that
increasing the spending in `newspaper` doesn't increase the sales, at least
when `radio` and `TV` are present.

**2. Carefully explain the differences between the KNN classifier and KNN
regression methods.**

KNN classifier estimates the conditional probability for some value to belong
to certain class, while KNN regression predicts the value of a variable.

**3. Suppose we have a data set with five predictors, X1 = GPA, X2 = IQ,
X3 = Gender (1 for Female and 0 for Male), X 4 = Interaction between
GPA and IQ, and X5 = Interaction between GPA and Gender. The
response is starting salary after graduation (in thousands of dollars).
Suppose we use least squares to fit the model, and get β̂0 = 50, β̂1 =
20, β̂2 = 0.07, β̂3 = 35, β̂4 = 0.01, β̂5 = −10.**

*(a)*

Model: `Y = 50 + 20*gpa + 0.07*iq + 35*gender + 0.01*gpa*iq - 10*gpa*gender`
Males: `Y = 50 + 20*gpa + 0.07*iq + 0.01*gpa*iq`
Females: `Y = 85 + 10*gpa + 0.07*iq + 0.01*gpa*iq`

Correct answer is iii. Solving the inequality for `gpa`

```
Ymales > Yfemales
50 + 20*gpa + 0.07*iq + 0.01*gpa*iq > 85 + 10*gpa + 0.07*iq + 0.01*gpa*iq
```

Shows that `gpa > 35/10`: starting salary is greater for males provided that
`gpa` is equal or greater than 3.5

*(b)*

```
Y = 50 + 20 * 4 + 0.07 * 110 + 35 + 0.01 * 4 * 110 - 10 * 4
```

Salary: 137.1k.

*(c)*

False, because GPA and IQ are in very different scales. Because IQ is in larger
scale, it's coefficient is `0.07`, and that doesn't mean there's no interaction.

**4. I collect a set of data (n = 100 observations) containing a single
predictor and a quantitative response. I then fit a linear regression
model to the data, as well as a separate cubic regression, i.e. Y =
β0 + β1 X + β2 X 2 + β3X 3 + e.** 

*(a)*

RSS of training set will be lower for the cubic regression despite the true 
relationship being linear, because cubic regression will also fit the noise and
randomness.

*(b)*

For the test set (i.e. unseen data during the model fit), instead, error would
be lower for the linear regression, because of the high variance of the cubic
regression due to the overfit of the test data, generalizing worse than the
linear model.

*(c)*

Train RSS will be lower for cubic regression than for linear regression always.

*(d)*

It's hard to tell without knowing to what extempt the true function is non
linear, but if it's far from linear, the RSS would be lower for the cubic
regression due to the high bias of the linear model; instead, if it's closer
to linear, the RSS would probably be lower for the linear regression due to
the high variance of the cubic model.

**6. Using (3.4), argue that in the case of simple linear regression, the
least squares line always passes through the point (x̄, ȳ).**

In the linear model, substutiting x with x̄, results in y = ȳ.

**7. It is claimed in the text that in the case of simple linear regression
of Y onto X, the R2 statistic (3.17) is equal to the square of the
correlation between X and Y (3.18). Prove that this is the case. For
simplicity, you may assume that x̄ = ȳ = 0.**

(In paper)
