--- 
title: "All About R and R Applications"
author: "Faizan Khalid Mohsin"
date: "2022-06-27"
site: bookdown::bookdown_site
output: bookdown::gitbook
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
github-repo: rstudio/bookdown-demo
description: "This is a minimal example of using the bookdown package to write a book. The output format for this example is bookdown::gitbook."
---

# Prerequisites

Placeholder



<!--chapter:end:index.Rmd-->

# Introduction {#intro}


Hello Everyone! Hope you all are doing well. 

I hope to help you become a data scientist through this book that you would otherwise need to learn to become by being hired and trained at a machine learning company. 


This book's examples and specific code is run on a window's operating system and is done using R. 






<!--chapter:end:01-intro.Rmd-->


# Overview

Placeholder



<!--chapter:end:02-overview.Rmd-->

# R Programming Techniques


## R Programming Essential Tips 

1. When repeating mutate to create for example percentage column in a table simply write that as a pip compatible function and call the function. 

2. Also, write small chucks of code and run it to see if it works. It will be much easier to debug if there is an error and to find and isolate it. It becomes very difficult to debug code the bigger it gets.


## Basics of R

### Print a string.

```r
print("First R lesson.")
```

```
## [1] "First R lesson."
```
### print a integer Value.


```r
print(23)
```

```
## [1] 23
```

### Print with variable.


```r
x <- "First R lesson."
x
```

```
## [1] "First R lesson."
```

### Print String with varibale.


```r
x <- "First"
cat(x, "R lesson.")
```

```
## First R lesson.
```

```r
sprintf("%s R lesson.",x)
```

```
## [1] "First R lesson."
```

## Assign variables

### Using = operator.


```r
x = 23
x
```

```
## [1] 23
```

### Using <- operator.



```r
x <- "First program."
x
```

```
## [1] "First program."
```

### Using -> operator.



```r
"First Program." -> x
x
```

```
## [1] "First Program."
```

### Multiple assignments


```r
x<- y<- 23
x
```

```
## [1] 23
```

```r
y
```

```
## [1] 23
```


## Wrting Basic functions.


```r
f_Name <- function (argument) {
statement
}
```

### Function  for x power y


```r
power <- function(x, y) {
  p <- x^y
print(paste(x,"raised to the power", y, "is", p))
}
```

### Example


```r
power(4,3)
```

```
## [1] "4 raised to the power 3 is 64"
```

## Working with libraries.

Libraries have multiple functions that have specific instructions to perform tasks.
 
### How to install packages. 



```r
#install.packages()
```


## Plots with ggplot


```r
library(ggplot2)
head(iris)
```

```
##   Sepal.Length Sepal.Width Petal.Length Petal.Width Species
## 1          5.1         3.5          1.4         0.2  setosa
## 2          4.9         3.0          1.4         0.2  setosa
## 3          4.7         3.2          1.3         0.2  setosa
## 4          4.6         3.1          1.5         0.2  setosa
## 5          5.0         3.6          1.4         0.2  setosa
## 6          5.4         3.9          1.7         0.4  setosa
```

### Barplot


```r
ggplot(data = iris, aes(x = Sepal.Length, y = Species)) +
    geom_bar(stat= "identity")
```

<img src="bookdown-demo_files/figure-html/unnamed-chunk-14-1.png" width="672" />
### point with ggplot2.


```r
plot <- ggplot(data = iris, aes(x = Sepal.Length, y = Species)) 
    plot+
    geom_point()
```

<img src="bookdown-demo_files/figure-html/unnamed-chunk-15-1.png" width="672" />

### Boxplot with ggplot2


```r
plot+
  geom_boxplot()
```

<img src="bookdown-demo_files/figure-html/unnamed-chunk-16-1.png" width="672" />


<!--chapter:end:03-rprogramming.Rmd-->


# Exploratory Data Analysis {#eda}

Placeholder


## Read the Data into the Programming Language
### Data Forms: Long format vs. Wide format
## Basic EDA Steps
### Step 1
### Step 2

<!--chapter:end:06-eda.Rmd-->

# General Useful Tips {#tips}

## Correct Writing


First of all, I want to start by Titles. It is very important that you know how titles are written properly. You need to title you analysis, visualization, applications, sections, everything correctly. 

Every first letter in a title should be capitalized except for prepositions or connecting words like and, or, the, this. 
If we want to convert the phrase general useful tips to a title it becomes: General Useful Tips. 

Now, also, sentences should be written properly. The first word's first letter should be capital and the sentence should end with a period also called full-stop like this one. 

## Essential Survival Habits.

One great thing I find about R Markdown and knitting a document is that to successfully knit there needs to be zero errors. So this is a great way to check if there is any error in the code.

For working in R Markdown. Please knit the markdown after making small changes in the code so you know if there is an error and can isolate, correct, and debug it. If you write a lot of code and then knit and there is a error, even a very simple error can be very hard to find buried in code. 

Further, once it knits successfully, then the code needs to be immediately committed to git and push it to GitHub.

These two steps of knitting and pushing the code to GitHub should be like breathing. Done extremely often automatically and even without thinking. If you can you should make a short cut like TAB + G so that the the r markdown knits and if successful then commits and pushes to GitHub only prompting you to add a commit message.

## Good General Habits.

Another, important tip is to look at your visualizations and the summary tables and think if the numbers you get make sense. I will be very frank here, I typically try not to do this because I have to use my brain and think. And sometimes that is actually very mentally power consuming.  

<!--chapter:end:07-tips.Rmd-->


# Git and Git Hub {#git}

Placeholder


## Folder Organiztion
## The Command Line
## Essential Command Line Tips
## How to see which remote repository your local repository is linked to or more explicitely, it is fetching from and pushing to.
## Git Commands Summary

<!--chapter:end:08-git.Rmd-->


# R Markdown {#rmarkdown}

Placeholder


## R markdown general tips for reports.
#### i. Code blocks:
#### ii. Comments blocks:
#### i. To see both code and output on R Markdown, write code in between \```{r} and 
#### \``` 
#### ii. If we only want to see the output and not the code then write the code between \```{r, 
#### \ echo=FALSE } 
#### and 
#### \```
## This is written in Heading size 2. In html is h2.
### This is written in Heading size 3. In html is h3.
#### This is written in Heading size 4. In html is h4.
##### This is written in Heading size 5. In html is h5.
###### This is written in Heading size 6. In html is h6.
## Sample paragraph displaying R Markdown capabilities
## math example

<!--chapter:end:09-rmarkdown.Rmd-->


# Visualization {#viz}

Placeholder


## Essential Visualization Principals
## Writing Visualization Titles
## Bar Chart tips

<!--chapter:end:10-visualization.Rmd-->


# How to host website on Git Hub {#gitwebhost}

Placeholder



<!--chapter:end:11-hosting_site_on_github.Rmd-->


# Python {#python}

Placeholder


## Basics of Python
## Data Analysis with Python Using Pandas
### Step 1
### Step 2

<!--chapter:end:12-python.Rmd-->


# Machine Learning {#ml}

Placeholder


## Machine Learning Overview
## Machine Learning Coding Conventions
## Important Ideas and Interview Questions

<!--chapter:end:18-ml.Rmd-->

# Applications

Some _significant_ applications are demonstrated in this chapter.

## Example one

## Example two

<!--chapter:end:19-applications.Rmd-->


# References {-}


<!--chapter:end:20-references.Rmd-->

# Final Words

We have finished a nice book.

<!--chapter:end:99-summary.Rmd-->
