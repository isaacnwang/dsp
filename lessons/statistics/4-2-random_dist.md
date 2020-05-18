[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

First I generated 1000 random numbers between 0 and 1.

random_sample = np.random.random(1000)

Next I tried to plot this sample on a PMF. 

sample_pmf = thinkstats2.Pmf(random_sample)
thinkplot.Pmf(sample_pmf)

You can't tell anything from this graph. So I plotted it on a CDF instead. 

random_cdf = thinkstats2.Cdf(random_sample)
thinkplot.Cdf(random_cdf)
thinkplot.Config(xlabel='Percentile rank', ylabel='CDF')

It's a much nicer looking graph. You can tell it is normally distributed because of the linear line from the CDF.
