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
![Mean Annual Wage by US State](https://github.com/user-attachments/assets/7ef0450e-5ef2-42d9-bf61-dcfd32183016)

![Top 5 and Bottom 5 States by Annual Mean Wage](https://github.com/user-attachments/assets/f9af7e28-edf0-426a-a4b1-82a57d86ce5a)
> The East and West Coasts show the highest mean wages, exceeding $20,000 more than central and sourthern states

### Gap Between Mean and Median Wages
![States with the Largest and Smallest Gaps Between Mean and Median Wages](https://github.com/user-attachments/assets/74696b4e-7ae0-4e9c-8376-40780af1e4ea)
> California, New York, and D.C. display the largest gaps, highlighting skewed income distributions

### Main Occupations For High and Low Income States
![Top Occupations by Employment Share in High and Low Income States](https://github.com/user-attachments/assets/c9facb64-2ea4-4a47-87c7-63534e5b46af)
> Across high and low income states, the distribution of main occupations does not differ with similar levels of employment for office and Administrative Support, Sales and related occupations, and Transportation and Material Occupations


### Employment in California, New York, and D.C.
![Share of U S](https://github.com/user-attachments/assets/31f53c91-b297-43d5-ab2b-d290b0d1414d)
> CEOs, the second best paid position by annnual mean wage, are heavily concentrated in California, New York, and Washington D.C., with 37% of U.S. CEOs located in just these three regions
> 
> Low wage positions also show high concentration in these states, highlighting the coexistence of income extremes

## Regression Analysis

### Research question
> We have seen that among the highest states with an annual mean wage, there seems to also be a high disparity between mean and median wages. Policies tend to focus on always trying to improve the average wage per state, but does that equal to a good growth for the state? Or does this create further inequality? we set to use the difference between mean and median as our dependent variable to see if increase in annual mean lead to growth in our dependent variable.

### Regression Results
> Our initial result emphasized that there is truly a relationship and that we can confidently reject the hypothesis that an increase in annual mean wage does not increase the gap between mean and median wage.
> 
> However, our model did not fully met the assumptions of regression. While there was a linear relationship, there was some mild heteroskedasiticy with greater variance for certain data points.
> 
> Additionally, while there was a slight skew at the tails, we can assume that there is normality. That being said, we will remove points that have been highlighted to distort the model and re run to see if our results still hold true
>
> After removing California, New York, and DC, and re running our simple linear model, our relationship was still statistically significant at the 99% confidence level. Our results highlighted that a $1 increase in mean wage is associated with a **$0.34 increase in wage gap**


##Conclusion and Recommendations 
