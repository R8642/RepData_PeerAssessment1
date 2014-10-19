---
title: "Reproducible Research: Peer Assessment 1"
author: "Rachel Tan"
date: "Sunday, October 19, 2014"
output: html_document
---
# Reproducible Research: Peer Assessment 1


library(knitr)
knit2html("PA1_template.Rmd")

## Loading and preprocessing the data

### 1.  Load the data 

```r
data <- read.csv("activity.csv")
```

### 2.  Process/transform the data (if nec) into a format suitable for analysis 
###     - convert the date to desired format

```r
data$date <- as.Date(data$date,format="%Y-%m-%d")
```

## What is mean total number of steps taken per day? 

```r
tot_steps <- sum(data$steps,na.rm=TRUE)
tot_steps
```

### 1.  Make a histogram of the total number of steps taken each day


```r
hist(aggregate(data$steps,list(data$date),FUN=sum, na.rm=T)$x,breaks=50)
```






### 2.  Calculate and report the mean and median 

2. total number of steps taken per day



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
