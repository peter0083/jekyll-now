---
layout: post
title:  "A R Visualization Exercise"
date:   2016-11-23
excerpt: "practice makes perfect"
project: true
tag:
- R
- viz
- ggplot2
- RStudio
comments: false
---


================
Peter Lin


November 22, 2016

    ##
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ##
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ##
    ##     intersect, setdiff, setequal, union

    ## Warning: package 'ggplot2' was built under R version 3.3.2

Introduction
------------

The Visualization user testing survey A and B were created. These two surveys were completed by 22 MDS students and 1 MDS TA in one lab session. Viz A (histogram) was designed with the intent of using it to detect distributions. Viz B (scatter plot) was designed with the intent of using it to identify outliers. This link is for [Survey A](https://docs.google.com/forms/d/e/1FAIpQLSeLOe0wiytisik6m06MnWuxhBP90fR7_YB7DKJPI7xcCJpdHA/viewform) and this link is for [Survey B](https://docs.google.com/forms/d/e/1FAIpQLSdRq499kEpBPGL-c24-cDD31DRtaBJvNXzn3DbXhg7NDaHWbw/viewform). To minimize the impact of answering first survey influencing the outcome of answering the second survey. The responses were collected and compiled into .csv files. The data was then loaded into data frame for exploratory data analysis.

    ## Warning: NAs introduced by coercion

    ## Warning: NAs introduced by coercion

    ##  [1]  3  2  1  1  1  1  2  2  2  1 NA  1  2  2 NA 20  1  2  0 NA  2  5  1

    ## 'data.frame':    46 obs. of  14 variables:
    ##  $ time               : Factor w/ 44 levels "17/11/2016 14:06:36",..: 1 2 3 4 5 6 7 8 9 10 ...
    ##  $ distrbtn_rating    : int  5 3 4 2 1 3 5 5 4 2 ...
    ##  $ outlier_rating     : int  5 3 4 5 4 5 2 5 3 4 ...
    ##  $ trend_rating       : int  5 3 3 3 2 4 4 5 3 4 ...
    ##  $ avg_walk_est       : num  4 3.5 6 4 4 8 5 2.5 NA 4.5 ...
    ##  $ distrbtn_walk      : Factor w/ 4 levels "Binomial","Exponential",..: 4 2 2 2 2 2 2 4 3 4 ...
    ##  $ distrbtn_homerun   : Factor w/ 4 levels "Binomial","Exponential",..: 2 3 2 2 2 2 2 4 3 4 ...
    ##  $ outlier_walk_est   : num  1 25 2 4 1 1 1 2.5 60 1 ...
    ##  $ outlier_homerun_est: int  1 13 4 2 1 1 1 1 90 5 ...
    ##  $ mode_walk_est      : chr  "5" "3" "3" "3" ...
    ##  $ mode_homerun_est   : int  10 13 7 10 19 55 18 10 20 10 ...
    ##  $ min_walk_est       : int  0 0 0 0 0 0 0 0 0 0 ...
    ##  $ min_homerun_est    : int  0 0 0 0 0 0 0 0 0 0 ...
    ##  $ index              : chr  "B" "B" "B" "B" ...

Findings from Exploratory Data Analysis
---------------------------------------

A.  Rating-type questions where students were to rate on a scale of 1 to 5 and distribution-matching questions with answers in drop-down menus were all well participated without any extraneous answers. Estimation-type questions where students were to enter a response was not well received. A mixture of text and numeric answers was collected. Text answers were replaced with "NA" to ensure unity of data type for analysis.

B.  The question that asked "making it easy to see the distribution of the data" gives a clustered response among 3, 4, and 5 with most response in 5 for survey A. The response from survey B are more evenly distributed.
![alt text](assets/img/r-viz/plot2-1.png)

Using Wilcoxon test, p-value is 0.000174, less than 0.05. The difference in response between survey A and B for question 2 is statistically significant. In other words, students feel that there is a difference in determining distribution when inspecting two visualizations: scattered plot vs histograms.

C.  The question that asked "making it easy to identify outliers" gives a clustered response among 2, 3, 4, and 5 in survey 5. The response from survey A are more evenly distributed.
![alt text](assets/img/r-viz/plot3-1.png)

Using Wilcoxon test, p-value is 0.00852, less than 0.05. The difference in response between survey A and B for question 2 is statistically significant. In other words, students feel that there is a difference in estimating the outlier between two visualizations, scattered plot vs histograms.

D.  Many distractor questions, such as mean and modes, that do not ask about outliers and distributions have demonstrated difference between scattered plot and histograms. However, they are do not suggest a difference in detecting outliers or distributions.

Conclusion and Discussion
-------------------------

1.  Based on the analysis of seven key questions, there are two questions that showed a difference between scattered plot vs histograms in detecting distribution and outliers. It is not strong enough to conclude that the students truly feel there is a difference between the two plots.

2.  The inability to show a major difference from the two surveys may be due to the lack of an answer key for reference. If this survey were conducted as a quiz and the result were evaluated against an answer key, the difference might have been more prominent. The fact that surveys are not graded may contribute to poor and unthoughtful answers that blurred the true difference. Also, maybe the visualization graphs given did not show a major distinction that make the differece obvious.

3.  Multiple-choice questions are better evaluated and show difference compared to open-ended questions where students can input either integers or numeric answers. For future surveys, multiple-choice questions are recommended to improve overall data quality and standardization.

4.  Further investigation is required to demonstrate the true difference in students' perception of scatter plot and histogram. More funding from the BC government for the MDS program will help investigators to increase sample size and improve study designs for better study outcomes.
