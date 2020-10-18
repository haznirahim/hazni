---
title: "My Analysis"
author: "hazni"
date: "10/18/2020"
output: 
  html_document: 
    keep_md: yes
---


# What do I need to do?

I will type these texts inside my Rmd file. 

I will pay attention to the symbols and the outputs.

I will remember to save this file constantly.

I will note the error message if any. 

# This is my first heading

And these are bullets:

- bullet1
- bullet2
- bullet3

## This is my second heading

This is **bold** and this is *italic*

### This is my third heading


```r
mydata <- mtcars
head(mydata)
```

```
##                    mpg cyl disp  hp drat    wt  qsec vs am gear carb
## Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
## Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
## Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
## Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
## Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2
## Valiant           18.1   6  225 105 2.76 3.460 20.22  1  0    3    1
```

And now I will show data summary


```r
summary(mydata)
```

```
##       mpg             cyl             disp             hp       
##  Min.   :10.40   Min.   :4.000   Min.   : 71.1   Min.   : 52.0  
##  1st Qu.:15.43   1st Qu.:4.000   1st Qu.:120.8   1st Qu.: 96.5  
##  Median :19.20   Median :6.000   Median :196.3   Median :123.0  
##  Mean   :20.09   Mean   :6.188   Mean   :230.7   Mean   :146.7  
##  3rd Qu.:22.80   3rd Qu.:8.000   3rd Qu.:326.0   3rd Qu.:180.0  
##  Max.   :33.90   Max.   :8.000   Max.   :472.0   Max.   :335.0  
##       drat             wt             qsec             vs        
##  Min.   :2.760   Min.   :1.513   Min.   :14.50   Min.   :0.0000  
##  1st Qu.:3.080   1st Qu.:2.581   1st Qu.:16.89   1st Qu.:0.0000  
##  Median :3.695   Median :3.325   Median :17.71   Median :0.0000  
##  Mean   :3.597   Mean   :3.217   Mean   :17.85   Mean   :0.4375  
##  3rd Qu.:3.920   3rd Qu.:3.610   3rd Qu.:18.90   3rd Qu.:1.0000  
##  Max.   :4.930   Max.   :5.424   Max.   :22.90   Max.   :1.0000  
##        am              gear            carb      
##  Min.   :0.0000   Min.   :3.000   Min.   :1.000  
##  1st Qu.:0.0000   1st Qu.:3.000   1st Qu.:2.000  
##  Median :0.0000   Median :4.000   Median :2.000  
##  Mean   :0.4062   Mean   :3.688   Mean   :2.812  
##  3rd Qu.:1.0000   3rd Qu.:4.000   3rd Qu.:4.000  
##  Max.   :1.0000   Max.   :5.000   Max.   :8.000
```

The mean of **mpg** is 20.090625

# Make a plot and hide the R codes

Now I will plot a histogram but hide the R codes:


```r
library(lattice)
```

```
## Warning: package 'lattice' was built under R version 4.0.3
```

```r
xyplot(disp ~ hp, data = mydata)
```

![](my_analysis_files/figure-html/unnamed-chunk-3-1.png)<!-- -->


# Adding an image


![This is the caption for the R Logo](Rlogo.jpg)


# Creating table

This is how you create a simple table in markdown

1.  Left text align 

| var  | group     | n  | %  |
|------|-----------|----|----|
| Sex  | Male      | 50 | 50 |
|      | Female    | 50 | 50 |
| Race | Malay     | 70 | 70 |
|      | Non-Malay | 30 | 30 |

2. Centred 

|  var |   group   |  n |  % |
|:----:|:---------:|:--:|:--:|
|  Sex |    Male   | 50 | 50 |
|      |   Female  | 50 | 50 |
| Race |   Malay   | 70 | 70 |
|      | Non-Malay | 30 | 30 |


