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

### Wage Differences Across States
![Mean Wage by U S](https://github.com/user-attachments/assets/79fdc111-89df-48d5-8938-df159c355457)

![Top and Bottom State](https://github.com/user-attachments/assets/b69c893a-26b3-4e80-aa21-db0681da145a)

> The East and West Coasts show the highest mean wages, exceeding $20,000 more than central and sourthern states

### Gap Between Mean and Median Wages
![Mean minus Median](https://github.com/user-attachments/assets/80ed5695-45d3-4cde-a9fe-e06ed5ae8d33)
> California, New York, and D.C. display the largest gaps, highlighting skewed income distributions

### Employment in California, New York, and D.C.
![Share of Employment in top and bottom 5 jobs](https://github.com/user-attachments/assets/d3db8ad1-17a8-4bee-9322-18cbdc1c0156)
> CEOs, the second best paid position by annnual mean wage, are heavily concentrated in California, New York, and Washington D.C., with 37% of all U.S. CEOs located in just these three regions
> Low wage positions also show high concentration in these states, highlighting the coexistence of income extremes
