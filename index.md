---
title       : Miles per hour to Kilometers per hour Conversion
subtitle    : 
author      : Shawn K
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Overview

The Purpose of this application is to convert MPH to Kilometers. This simple but powerful app helps anyone in need of a quick conversion of MPH to Kilometers. 

--- .class #id 
## Sample Code
This shows how the calculation is being applied in the server.R file. 


```r
library(shiny)
library(UsingR)

mphToKilometers <- function(mph) {1.60934*(mph)}

shinyServer(
    function(input, output) {
        output$inputValue <- renderPrint({input$mph})
        output$prediction <- renderPrint({mphToKilometers(input$mph)})
    }
)
```

--- .class #id 

## Screenshot of App

<img src="shiny.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" width="600" />

--- .class #id 

## Code
Demostration of embedded R code that runs in slidify document


```r
x <- 78
y <- x * 2
print(y)
```

```
## [1] 156
```
