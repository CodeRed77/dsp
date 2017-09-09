[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> *Question*: Using the variable **totalwgt_lb**, investigate whether first babies are lighter or heavier than others.
Compute Cohen’s effect size to quantify the difference between the groups. How does it compare to the difference in pregnancy length?

Answer: To analyze this question, the first step is to extract the relevant data. In the code shown below, functions from the ThinkStats2 book are utilized.

```python

first_hist_wgt = thinkstats2.Hist(firsts.totalwgt_lb, label='first')
other_hist_wgt = thinkstats2.Hist(others.totalwgt_lb, label='other')

# Compute Mean and median
firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()
# first baby avg weight - 7.20 lbs
# other baby avg weight - 7.32 lbs

firsts.totalwgt_lb.median(), others.totalwgt_lb.median()
# first baby median weight - 7.31 lbs
# other baby median weight - 7.38 lbs
```

Computing the mean and median weight both suggests that first babies are slightly lighter than other babies. Next, Cohen's effect size is calculated between the groups.

```python

CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)

# value of -0.08 stdeviations suggests the difference is very small

```
The Cohen's effect size for total weight is -0.089 standard deviations, between the two groups. This is larger than the effect size for pregnancy length, which is 0.028. Both of these effect sizes are relatively small, suggesting little difference between first born babies and non-first borns for these two statistics.
