---
title       :  Basic Investment Strategy on Shiny
subtitle    : 
author      : c-spohrer
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## A Basic Investment Strategy 

A very traditional investment strategy divides your investments between stocks and bonds. This has the following benefits.


  1. Reduces volatitilty.
  2. Reduces maximum drawdown.
  3. However at the expense of lagging behind during bull markets. 

--- .class #id 

## S&P500 SPY Exchange Traded Fund

Monthly and annualized returns for the SPY ETF


```
[1] "SPY" "BND"
```

```
      Jan   Feb  Mar  Apr  May  Jun  Jul  Aug  Sep   Oct  Nov Dec   SPY
2008 -5.2  -2.6 -0.9  4.8  1.5 -8.4 -0.9  1.5 -9.4 -16.5 -7.0 1.0 -36.2
2009 -8.2 -10.7  8.3  9.9  5.8 -0.1  7.5  3.7  3.5  -1.9  6.2 1.9  26.3
2010 -3.6   3.1  6.1  1.6 -7.9 -5.2  6.8 -4.5  9.0   3.8  0.0 6.7  15.1
2011  2.3   3.5  0.0  2.9 -1.1 -1.7 -2.0 -5.5 -6.9  10.9 -0.4 1.0   1.9
2012  4.6   4.3  3.2 -0.7 -6.0  4.1  1.2  2.5  2.5  -1.8  0.6 0.9  16.0
2013  5.1   1.3  3.8  1.9  2.4 -1.3  5.2 -3.0  3.2   4.6  3.0 2.6  32.3
2014 -3.5   4.5  0.8  0.7  2.3  2.0   NA   NA   NA    NA   NA  NA   6.9
```


--- .class #id 

## Vanguard Bond Index BND Exchange Traded Fund

Monthly and annualized returns for the BND ETF


```
      Jan  Feb  Mar  Apr  May  Jun Jul  Aug  Sep  Oct  Nov  Dec
2008  1.3  0.1  0.4 -0.3 -1.0  0.0 0.0  0.8 -0.5 -2.9  3.9  5.2
2009 -2.1 -0.6  1.1  0.5  0.7  0.6 1.3  1.0  1.0  0.3  1.3 -1.5
2010  1.3  0.3 -0.2  1.1  1.1  1.4 0.9  1.6  0.0  0.3 -0.7 -1.0
2011  0.1  0.3 -0.2  1.5  1.2 -0.4 1.6  1.6  0.7  0.1 -0.1  1.2
2012  0.6  0.0 -0.5  1.1  0.9  0.1 1.2  0.2  0.2 -0.1  0.1 -0.9
2013 -0.7  0.5  0.1  1.0 -1.9 -1.6 0.4 -0.9  1.1  0.9 -0.3 -0.6
2014  1.6  0.5 -0.2  0.8  1.1 -0.5  NA   NA   NA   NA   NA   NA
     monthly.returns
2008             6.9
2009             3.6
2010             6.2
2011             7.9
2012             3.0
2013            -2.1
2014             3.3
```


--- .class #id 

## Monthly and annualized returns for a mix of SPY and BND ETF's

Here is the results of allocating 60% to the SPY etf, and 40% to the BND ETF, and rebalancing monthly.


```
      Jan  Feb  Mar Apr  May  Jun  Jul  Aug  Sep   Oct  Nov Dec annualized
2008 -2.6 -1.5 -0.4 2.7  0.5 -5.0 -0.5  1.3 -5.9 -11.1 -2.6 2.7      -21.0
2009 -5.8 -6.7  5.4 6.1  3.8  0.2  5.0  2.6  2.5  -1.0  4.2 0.6       17.3
2010 -1.7  2.0  3.6 1.4 -4.3 -2.5  4.4 -2.1  5.4   2.4 -0.3 3.6       12.0
2011  1.4  2.2 -0.1 2.3 -0.2 -1.2 -0.5 -2.6 -3.9   6.6 -0.3 1.1        4.6
2012  3.0  2.6  1.7 0.0 -3.2  2.5  1.2  1.6  1.6  -1.1  0.4 0.2       10.8
2013  2.8  1.0  2.3 1.6  0.6 -1.5  3.3 -2.1  2.3   3.1  1.7 1.3       17.5
2014 -1.5  2.9  0.4 0.7  1.8  1.0   NA   NA   NA    NA   NA  NA        5.5
```


--- .class #id 

## Interactive Shiny App


If you would like to play around with tweaking the percentage allocated to each fund, there is a Shiny app at:

http://spohrer.shinyapps.io/code

All you need to do is adjust the slider control to set the allocation to the SPY ETF between 0 and 100%, and see how the cumulative return varies over time, from Jan1, 2008, to June 19, 2014.

Have fun.

--- .class #id


