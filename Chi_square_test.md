# Chi Square Test

Author: Huanfa Chen

Date: 2021/05/18

## Introduction

There are two types of chi-square tests. Both use the chi-square statistic and distribution for different purposes:

1. **chi-square goodness of fit test**: determines if sample data matches a population or a distribution (i.e. a population with a normal distribution or one with a Weibull distribution)
2. **chi-square test for independence**: compares two variables in a contingency table to see if they are related. In a more general sense, it tests to see whether distributions of categorical variables differ from each other.

## Chi-Square Statistic

The formula for the chi-square statistic used in the chi square test is:

$\tilde{\chi}_c^2=\frac{1}{n}\sum_{k=1}^{n} \frac{(O_k - E_k)^2}{E_k}$

‘c’ stands for the degrees of freedom. and ‘O’ is the observed value and E is the expected value.

Note that this statistic can only be used on numbers, both `O` and `E` should be numbers. They can’t be used for percentages, proportions, means or similar statistical values. For example, if you have 10 percent of 200 people, you would need to convert that to a number (20) before you can run a test statistic.

You can use this formula for a contingency table.

A low value for chi-square means there is a high correlation between your two sets of data. 

In theory, if your observed and expected values were equal (“no difference”) then chi-square would be zero.

### Chi-Square Statistic for contingency table

Contingency tables (also called crosstabs or two-way tables) are used in statistics to summarize the relationship between several categorical variables. A contingency table is a special type of **[frequency distribution table](https://www.statisticshowto.com/probability-and-statistics/descriptive-statistics/frequency-distribution-table/)**, where two variables are shown simultaneously.

A chi-square statistic can be conducted on contingency tables to test whether or not a relationship exists between variables. These effects are defined as relationship between rows and columns.

![contingency](https://www.statisticshowto.com/wp-content/uploads/2013/07/contingency-300x289.jpg)

An example testing if sexual orientation is linked to contracting AIDS is as above.

However, the note under the results states that “4 cells (66.7%) have expected count less than 5.” Generally, if this is over 25%, the result could be due to chance alone. Therefore, the results from this particular test are **not statistically significant**.

In R, this test can be conducted using the [prop.test](https://github.com/SurajGupta/r-source/blob/master/src/library/stats/R/prop.test.R) function. This test is also called k-sample test for differences in proportions.

### Chi-Square distribution 

![chi square distribution](https://www.statisticshowto.com/wp-content/uploads/2014/11/chi-square-distribution-300x200.png)

The chi-square distribution (also called the chi-squared distribution) is a special case of the [gamma distribution](https://www.statisticshowto.com/gamma-distribution/); A chi square distribution with n [degrees of freedom](https://www.statisticshowto.com/probability-and-statistics/hypothesis-testing/degrees-of-freedom/) is equal to a gamma distribution with a = n / 2 and b = 0.5 (or β = 2).

Let’s say you have a [random sample](https://www.statisticshowto.com/probability-and-statistics/statistics-definitions/simple-random-sample/) taken from a [normal distribution](https://www.statisticshowto.com/probability-and-statistics/normal-distributions/). The chi square distribution is the distribution of the sum of these random samples **squared** . The **degrees of freedom (k)** are equal to the number of [samples ](https://www.statisticshowto.com/sample/)being summed. For example, if you have taken 10 samples from the normal distribution, then df = 10. The degrees of freedom in a chi square distribution is also its mean. In this example, the mean of this particular distribution will be 10. Chi square distributions are always [right skewed](https://www.statisticshowto.com/probability-and-statistics/skewed-distribution/#SkewRight). 

The greater the degrees of freedom, the more the chi square distribution looks like a normal distribution.

## Differences with ANOVA



## References

- https://www.statisticshowto.com/probability-and-statistics/chi-square/