[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

# Homework Question

Cohen’s D is an example of effect size. Other examples of effect size are: correlation between two variables, mean difference, regression coefficients and standardized test statistics such as: t, Z, F, etc. In this example, you will compute Cohen’s D to quantify (or measure) the difference between two groups of data.

You will see effect size again and again in results of algorithms that are run in data science. For instance, in the bootcamp, when you run a regression analysis, you will recognize the t-statistic as an example of effect size.

# Textbook Question

Using the variable `totalwgt_lb`, investigate whether first babies are lighter or heavier than others. Compute Cohen’s d to quantify the difference between the groups. How does it compare to the difference in pregnancy length?

# Solution

The Cohen's D measure is a difference in the means of two populations divided by their pooled standard deviation.

As shown in the following code, the effect is small (following Cohen's initial nomenclature). The negative effects comes from first children being -- on average -- lighter.

```
> firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()
(7.201094430437772, 7.325855614973262)
```

```
> CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
-0.08867292707260174
```