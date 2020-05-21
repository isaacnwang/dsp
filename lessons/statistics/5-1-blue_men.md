[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

First I used the given mean and standard deviation to set up a normal distribution.

mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)
type(dist)

Next I converted 5 foot 10 inches and 6 foot 1 inch to centemeters and used the CDF to find the area between 5'10 and 6'1.


short = dist.cdf(177.8)    # 5'10"
tall = dist.cdf(185.4)   # 6'1"
short, tall, tall-short

(0.48963902786483265, 0.8317337108107857, 0.3420946829459531)

About 34% of people qualify to audition for blue men group.
