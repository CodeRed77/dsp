[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> *Question:* In the BRFSS (see Section 5.4), the distribution of heights is roughly normal with parameters µ = 178 cm and σ = 7.7 cm for men, and µ = 163 cm and σ = 7.3 cm for women.

>> In order to join Blue Man Group, you have to be male between 5’10” and 6’1” (see http://bluemancasting.com). What percentage of the U.S. male population is in this range? Hint: use scipy.stats.norm.cdf.

To determine the probability of falling into the specified height range, the scipy stats library is imported. Then it is simply a matter of converting the height into the same unit of measurement (cm), and then computing the difference in CDF.

```python
import scipy.stats
mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)

# first convert feet into cm
lower = (5* 12 + 10) * 2.54
upper = (6 * 12 + 1) * 2.54

# Compute the difference in cdf to get the probability of being between the 5'10" and 6'1" range.
dist.cdf(upper) - dist.cdf(lower)

```

```python
0.34274683763147457
```
The probability of meeting the height requirements is approximately 0.34.
