---
title: "Information+Instructions"
author: "Samantha Davies"
date: "2025-05-15"
---




# Analysis of Factors Influincing Student Performance

This project determines factors that impact student performance on math
tests. Variables analyzed include various demographic factors. The
dataset used contains student scores in math, reading, and writing. Only
math scores were analyzed here. The analysis aims to identify trends and
relationships between student demographics and their academic
performance in order to be able to predict which students will need more
help and more studying ahead of test-time.

------------------------------------------------------------------------

## Softwear

This project is ran in R and RStudio. Many R libraries are used
throughout the analysis.

Ensure the required libraries are installed:

library(ggplot2) library(dplyr) library(tidyr) library(leaps)
library(car) library(lmtest)

## Instructions

1.  Open RStudio

2.  Open the R Markdown file Final_project.Rmd.

3.  Click the "Knit" button in RStudio to generate the analysis

    -   This will run the analysis and display all results.

## Analysis

This project involves a detailed analysis of the StudentsPerformance.csv
dataset. Steps were taken to ensure the analysis provides accurate,
useful results:

1.  Preparation - Data cleaning

    -   Handle missing values (though none were present)
    -   Ensure all data types were in correct format
    -   Prepare the dataset for analysis by creating 'data_clean'
        dataframe

2.  Exploratory Data Analysis

    -   Visualize distributions of key variables (math, reading, and
        writing scores)
    -   Visualize relationships between variables
        -   Note: here, I confirmed that the similarities in math,
            reading, and writing scores amonst students was not the
            important relationship to analyze, but rather the
            relationship between student demographics and any one test
            score would be more useful for determining farther in
            advance which students will struggle the most. I arbitrarily
            chose math score as the test score to focus on.

3.  Statistical modeling

    -   Multiple linear regression was used to analyze the impact of
        demographic factors on students' math scores

4.  Model evaluation

    -   The performance of the regression model was assessed

## Results

1.  Key findings:

    -   Parental education: Student whose parents have higher education
        levels tend to score better in math.

    -   Gender: Male students generally scored slightly higher in math
        compared to females.

    -   Test preparation courses: Students who completed a test
        preparation course performed better than those who did not

    -   Race/ethnicity: Students in some racial/ethnic groups performed
        significantly better than those in some other groups

    -   Lunch prices: Students who received reduced lunch performed
        worse on thier math tests than those who did not.

2.  The linear regression model showed that the predictors analyzed are
    not able to explain much of the variation in math test scores, with
    an adjusted R2 value of 0.23.

    ## Visualizations

    1.  Initial distribution checks
        -   Distribution of math, reading, and writing scores appear to
            be normal, with a few low outliers. All predictor variables
            are categorical, and their spreads are shown as well. A
            correlation of math, reading, and writing scores shows that
            all are closely relating to one another (strong
            multicolinearity), but this will not impact the analysis, as
            I was interested in determining one test score from
            non-academic predictor variables.
    2.  Regression assumptions verification
        -   Residuals vs fitted values were plotted and a Q-Q plot was
            created. Plots demonstrated that all assumptions made for
            this model were satisfied.

            See report for plots.

## Conclusions

The analyzed predictor variables are all important in determining a
student's math test score, and don't use any previous academic history
to do so.

This provides a good baseline understanding of how a students
demographics factor into their performance in school, and shows that it
is possible to create programs that target students whose background may
be limiting their abilities to succeed in school.

Programs based on this type of analyses should be implemented, and the
involved students should be analyzed before and after participating in
order to determine the effectiveness of such programs.

This analysis should be conducted on reading and writing scores as well
as math scores in case the predictors analyzed are better at predicting
reading or writing than math. If this were true, reading, writing, and
math are all very closely related, and it could be assumed that a
student who will need help in one subject wll also need help in other
subjects.
