---
title       : Tidyr App
subtitle    : Developing Data Products Project
author      : Michael Addonisio
job         : 
framework   : io2012   # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Tidy Shiny: Course Project
The Tidy Shiny app is a data wrangiling tool that allows the user to easily tranform data from "wide-to-long" and from "long-to-wide". It accomplishes this task primarily by using the the package 'tidyr' and its useful functions gather and spread. This app has four principal elements. 



1. Uploading - the app begins with a preloaded dataset for demo purposes
2. Gathering - allows user to transform data from "wide-to-long"
3. Spreading - allows user to tranform data from "long-to-wide"
4. Downloading - allows user to download transformed dataset in .csv format

--- .class #id 

## Gathering

To use the Gathering function, you choose the scale variables you would like to gather. Below you can see the first 5 rows of the transformation on the example dataset by choosing X, Y, and Z.



```
##         time         X          Y            Z
## 1 2009-01-01 0.5347014  2.8315960 -10.50664878
## 2 2009-01-02 0.1509189  0.9251856  -0.01670842
## 3 2009-01-03 0.6873994  1.5353982  -5.75031889
## 4 2009-01-04 0.5534994 -0.7711718  -1.05758055
```

```
##         time key     value
## 1 2009-01-01   X 0.5347014
## 2 2009-01-02   X 0.1509189
## 3 2009-01-03   X 0.6873994
## 4 2009-01-04   X 0.5534994
```

--- .class #id 

## Spreading

To use the Spreading function, you choose the scale variables you select the key and value variables that you would like to spread on. Below you can see the first 5 rows of the transformation on the created dataset from the last slide by choosing key and value variables. 



```
##         time key      value
## 1 2009-01-01   X  1.2697285
## 2 2009-01-02   X  0.2484924
## 3 2009-01-03   X -0.5003911
## 4 2009-01-04   X  0.4599079
```

```
##         time          X          Y          Z
## 1 2009-01-01  1.2697285 -1.3931461 -0.7252226
## 2 2009-01-02  0.2484924 -0.7521495 -5.4241407
## 3 2009-01-03 -0.5003911 -2.8913119  2.9247927
## 4 2009-01-04  0.4599079 -2.0991269  1.7447743
```

--- .class #id 

## Final Step

- Once you transform the data into your liking you can save the data using the download button
- Vuola! Your tidy dataset is ready to be analysed!!!
- Thank you, I hope you enjoy it!
