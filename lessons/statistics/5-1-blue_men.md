[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

# Homework Question

This is a classic example of hypothesis testing using the normal distribution. The effect size used here is the Z-statistic.

# Textbook Question

In the BRFSS (see The lognormal Distribution), the distribution of heights is roughly normal with parameters 178 cm and 7.7 cm for men, and 163 cm and 7.3 cm for women.

In order to join Blue Man Group, you have to be male and between 5′10″ and 6′1″ tall. What percentage of the US male population is in this range? Hint: use scipy.stats.norm.cdf.

# Solution

According to the BRFSS data, **~35%** of American males fulfill the Blue Man Group height requirements.

```
mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)

low = dist.cdf(177.8)    # 5'10"
high = dist.cdf(185.4)   # 6'1"
```

```
> high-low
0.3420946829459531
```