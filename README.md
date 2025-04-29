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
We observed that among states with the highest annual mean wages, there also appears to be the greatest disparity between mean and median wages.  

Policies often focus on improving the average wage per state, but does that translate to overall economic improvement? Or could it lead to greater inequality?

To explore this, we used the difference between mean and median wage as our dependent variable, aiming to understand if increases in annual mean wage drive wage inequality.

### Regression Results
Our initial model emphasized that a relationship exists, and we can confidently reject the hypothesis that increases in mean annual wage do not contribute to the wage gap.

However, our model did not fully met the assumptions of linear regression. While there was a linear relationship, there was some mild heteroskedasiticy with greater variance for certain data points.

Additionally, while there was a slight skew in the tails of our QQ-plot, the assumption of normality meets. That being said, we removed the observations that have been identified as disproportionately influential and and re-ran our model to test for robustness.

After removing California, New York, the relationship remained statistically significant at the 99% confidence level. A **$1 increase** in mean wage is associated with a **$0.34 increase in the wage gap**.


## Conclusion

- States with high annual mean wages are associated with greater wage inequality
- California, New York, and D.C. have a large proportion of the highest-paying occupations (e.g., CEOs), while also sharing a significant portion of the lowest-paying jobs.  
- Aiming to improve annual mean wage will not necessarily improve the standard of living for most residents. Policies should focus on addressing inequality at the **lower end** of the income distribution.

## Recommendations
- Work to raise minimum wages to minimize the gap between the annual mean wage and annual median wage
- Expand social programs to improve access to education and job training, particularly for underserved communities
