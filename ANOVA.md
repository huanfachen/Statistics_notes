# ANOVA

ANOVA (Analysis of variance) is a collection of statistical models and their associated estimation procedures (such as the "variation" among and between groups) used to analyze the differences among means. 

ANOVA was developed by Ronald Fisher.

ANOVA is based on the law of total variance, where the observed variance in a particular variable is partitioned into components attributable to different sources of variation.

In its simplest form, ANOVA provides a statistical test of whether two or more population means are equal, and therefore generalizes the t-test beyond two means.

**In ANOVA, there are many instances that are divided into n groups of an independent variable (or multiple independent variables). Then you want to test whether the mean in different groups are statistically equal.**

The target variable (aka dependent variable) in ANOVA should be a continuous variable.

## One-way or two-way ANOVA

One-way or two-way refers to the number of independent variables (IVs) in the ANOVA test.

- One-way has one IV (with two groups). For example: a manufacturer has two different processes to make light bulbs. They want to know if one process is better than the other.
- Two-way has two independent variable (it can have multiple levels). 

Groups or levels are different groups within the same independent variable.

If your groups or levels have a hierarchical structure (each level has unique subgroups), then use a nested ANOVA for the analysis.

## One-way ANOVA

A one way ANOVA is used to compare two means from two or more independent (unrelated) groups using the **F-distribution**. The null hypothesis for the test is that the two means are equal. Therefore, a significant result means that the two means are unequal.

Limitations of a one-way ANOVA. A one way ANOVA will tell you that at least two groups were different from each other. But it won’t tell you which groups were different. If your test returns a significant f-statistic, you may need to run an ad hoc test (like the Least Significant Difference test) to tell you exactly which groups had a difference in means.

## Two-way ANOVA

If your experiment has a quantitative outcome and you have two categorical explanatory variables, a two way ANOVA is appropriate. For example, you might want to find out if there is an interaction between income and gender for anxiety level at job interviews. The anxiety level is the outcome, or the variable that can be measured. Gender and Income are the two categorical variables. These categorical variables are also the independent variables, which are called factors in a Two Way ANOVA.

## Can ANOVA be used for ordinal target variable?

The answer is that for all practical purposes, you can do so. See this post: https://www.researchgate.net/post/What_is_the_most_suitable_statistical_test_for_ordinal_data_eg_Likert_scales

Reference: de Winter, J. and D. Dodou (2010), Five-Point Likert Items: t test versus Mann-Whitney-Wilcoxon, Practical Assessment, Research & Evaluation, Vol 15, No 11.

Alternatives are Mann-Whitney U test (for comparing two groups) or Kruskal–Wallis H test (for comparing three or more groups).

## References

- https://www.statisticshowto.com/probability-and-statistics/hypothesis-testing/anova/#ANOVA
- 
