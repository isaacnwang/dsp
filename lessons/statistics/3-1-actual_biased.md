[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

First I constructed a histogram to visualize the distribution of the number of children.

  resp = nsfg.ReadFemResp()

  hist2 = thinkstats2.Hist(resp.numkdhh, label='Num of Children')
  thinkplot.Hist(hist2)
  thinkplot.Config(xlabel='Number of Children under 18', ylabel='Count')

Next I converted this distribution to a PMF by creating a PMF object. 

  pmf2 = thinkstats2.Pmf(resp.numkdhh, label='Num of Children')
  
I then created a histogram and PMF of my new PMF and to visualize my new distribution.

  thinkplot.Hist(pmf2)
  thinkplot.Config(xlabel='Number of Children', ylabel='Pmf')
  
  thinkplot.Pmf(pmf2)
  thinkplot.Config(xlabel='Number of Children', ylabel='Pmf')
  
After seeing these visualizations, I computed the biased distribution I would see if I surveyed the children and asked them how many children under 18 (including themselves) are in their household.

  biased_pmf2 = BiasPmf(pmf2, label='observed')
  
Finally, I plotted both the actual and biased distribution and computed their means.
  
  thinkplot.PrePlot(2)
  thinkplot.Pmfs([pmf2, biased_pmf2])
  thinkplot.Config(xlabel='Number of Children', ylabel='PMF')
  
  print('Actual mean', pmf2.Mean())
  print('Observed mean', biased_pmf2.Mean())
  
 
