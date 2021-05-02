**1. Using a little bit of algebra, prove that (4.2) is equivalent to (4.3). In
other words, the logistic function representation and logit represen tation for
the logistic regression model are equivalent.**

(In paper)

**2. It was stated in the text that classifying an observation to the class
for which (4.12) is largest is equivalent to classifying an observation
to the class for which (4.13) is largest. Prove that this is the case. In
other words, under the assumption that the observations in the kth
class are drawn from a N (μk , σ 2 ) distribution, the Bayes’ classifier
assigns an observation to the class for which the discriminant function
is maximized.**

(In paper)

**3. This problem relates to the QDA model, in which the observations
within each class are drawn from a normal distribution with a class-
specific mean vector and a class specific covariance matrix. We con-
sider the simple case where p = 1; i.e. there is only one feature.
Suppose that we have K classes, and that if an observation belongs
to the kth class then X comes from a one-dimensional normal dis-
tribution, X ∼ N (μk , σk 2 ). Recall that the density function for the
one-dimensional normal distribution is given in (4.11). Prove that in
this case, the Bayes’ classifier is not linear. Argue that it is in fact
quadratic.**

**4.  When the number of features p is large, there tends to be a deteri-
oration in the performance of KNN and other local approaches that
perform prediction using only observations that are near the test ob-
servation for which a prediction must be made. This phenomenon is
known as the curse of dimensionality, and it ties into the fact that
non-parametric approaches often perform poorly when p is large. We
will now investigate this curse.**

* (a) If the data is uniformly distributed, 10%
* (b) 10% of 10%: 1%
* (c) 0.1 ^ 100
* (d) As seen in the previous respones, as the number of predictors increase,
the fraction of data used tends to 0
* (e)
  * p = 1: 0.1 (single dimention)
  * p = 2: 0.1 ^ (1/2) = 0.31
  * p = 100:  0.1 ^ (1/100) = 0.977

**5. We now examine the differences between LDA and QDA.**

* (a) If the Bayes decision boundary is linear, QDA would anyways perform 
better on the training set as it's more flexible and it would also capture the
noise and randomness, however it would generalize worse so the LDA would
perform better on the test set.

* (b) For non linear decision boundary, QDA would perform better on both
training and test set, as the LDA suffers from higher bias.

* (c) We would generally expect a more flexible function to perform better with
a large number of samples as the variance would be less, however this also
depends on the underlaying true function; if it's strictly linear, then
probably a really great number of samples would be required for QDA to
outperform LDA.

* (d) False, QDA would fit a more flexible function suffering from higher
variance, that is, it would perform worse with the unseen test data. Otherwise,
we would just always fit the more flexible method for any problem.

**6. Suppose we collect data for a group of students in a statistics class
with variables X1 = hours studied, X2 = undergrad GPA, and Y =
receive an A. We fit a logistic regression and produce estimated
coefficient, β̂0 = −6, β̂1 = 0.05, β̂2 = 1.**

* (a) Plugging the coefficients and parameters in the logistic regression
yields 0.377
* (b) Resolving the equation for `X1` yields 50 hours (done in paper)

**7.  Suppose that we wish to predict whether a given stock will issue a
dividend this year (“Yes” or “No”) based on X, last year’s percent
profit. We examine a large number of companies and discover that the
mean value of X for companies that issued a dividend was X̄ = 10,
while the mean for those that didn’t was X̄ = 0. In addition, the
variance of X for these two sets of companies was σ̂ 2 = 36. Finally,
80 % of companies issued dividends. Assuming that X follows a nor-
mal distribution, predict the probability that a company will issue
a dividend this year given that its percentage profit was X = 4 last
year.**

* Prior probabilities: 0.8 for `yes` and 0.2 for `no`
* Calculate the `yes` and `no` probability for `X = 4` plugging the values
in the probability density function
* Plug the values in the Bayes classifier, yields ~`75%`

**8. Suppose that we take a data set, divide it into equally-sized training
and test sets, and then try out two different classification procedures.
First we use logistic regression and get an error rate of 20 % on the
training data and 30 % on the test data. Next we use 1-nearest neigh-
bors (i.e. K = 1) and get an average error rate (averaged over both
test and training data sets) of 18 %. Based on these results, which
method should we prefer to use for classification of new observations?
Why?**

The training error for KNN with K=1 is just 0, as every training sample will
just choose itself. This means that the test error is 36%, if the averaged
error is 18%. So logistic regression would be a better choice.

**9. This proble has to do with odds.**


