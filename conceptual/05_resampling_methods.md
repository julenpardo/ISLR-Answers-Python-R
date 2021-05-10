**1.  Using basic statistical properties of the variance, as well as single-
variable calculus, derive (5.6). In other words, prove that α given by
(5.6) does indeed minimize Var(αX + (1 − α)Y ).**

Done in paper (5.6 should be integrated, not derivated; or derived `Var(αX + (1 − α)Y)`).
Expand `Var(αX + (1 − α)Y)` based on the property of variance, derive wrt α,
equalize to 0 (as it's the min value), and resolve for α, resulting in equation
5.6.

**2.  We will now derive the probability that a given observation is part
of a bootstrap sample. Suppose that we obtain a bootstrap sample
from a set of n observations.**

* (a) For n observations, the probability that it is is 1/n, so the probability
that it's not is 1 - 1/n
* (b) Same as above
* (c) Because the probability of an observation of not being in the bootstrap
sample, is the product of the probability of every observation not being in the
sample
* (d) Using the formula above, and subtracting from 1 as it's the probability that
it's in the bootstrap sample, `1 - ((1 - 1/5)^5)` = 0.67232
* (f) Same, `1 - ((1 - 1/100)^100)` = 0.634
* (g) The probability asymptotes at ~0.632 as n tends to infinite
* (h) Result is 0.6422, pretty close the the value the function asymptotes at.
This is regardless what index the j-th observation is. For larger n, the value
will be closer to ~0.632

**3. We now review k-fold cross-validation.**

* (a) k-fold cross-validation is implemented by randomly dividing the dataset
into equally sized k groups (a usual value for k is 10). On every i iterations
for a total of k iterations, the k-i-th fold is used as the test set, for which
the test error is calculated, and being the model fit with the rest of folds.
The final error of the k-fold CV is the mean of the calculated test errors.
* (b)
  * i. Advantage relative to validation set approach: less variability in
   error, the model is fit with all the data. The disadvantage is that k models
   are fit vs a single one, being mroe demanding computationally.
  * ii. Advantage relative to LOOCV: computationally more efficient (as long as
  k < n), lower variance. Disadvatanges: higher bias (less data used for fitting
  the model)


**4.  Suppose that we use some statistical learning method to make a pre-
diction for the response Y for a particular value of the predictor X.
Carefully describe how we might estimate the standard deviation of
our prediction.**

We can use bootstrap with replacement. We generate _B_ boostrap models (for a
large _B_), use each of those to make a prediction for the predictor X, and
then calculate the standard error for each of these predictions with the formula
given in 5.8 (page 189).
