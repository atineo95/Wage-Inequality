# Wage Inequality Across U.S. States: An Analysis of Mean and Median Wage Gaps

## Introduction
Wage inequality is a growing issue across and within U.S. states. This project explores how annual mean wages vary across states, what occupations drive these differences, and whether increasing mean wages lead to greater income inequality within states.

## Data Overview
- Source: Occupational Employment and Wage Statistics (OEWS) Survey - Bureau of Labor Statistics 
- Variables: State, Annual Mean Wage, Annual Median Wage, Total Employment, Occupation titles

## Project Workflow

- **Cleaned data** — Handled missing values and converted variable types to numeric
- **Performed exploratory data analysis (EDA)** — Compared wages across states, analyzed wage gaps, and reviewed occupational breakdowns
- **Ran weighted simple linear regression** — Used `total_emp` to weight states by employment size, modeling wageGap ~ a_mean
- **Validated model assumptions and removed influential states** — Evaluated regression assumptions (linearity, independence, normality, Homoscedasticity), then removed high-leverage states (D.C., NY, CA) to test model robustness.

## Exploratory Data Analysis

