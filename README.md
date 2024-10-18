# Money and Banking Analysis
## This is a project that proves and visualizes macroeconomic theories for Money &amp; Banking

## Table of Contents
- [Tool](#tool)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Sources](#data-sources)
- [Results and Findings](#results-and-findings)
  - [1. What is the relationship between real and nominal GDP](#1-what-is-the-relationship-between-real-and-nominal-gdp)
  - [2. Effect of the COVID-19 Pandemic on Inflation](#2-effect-of-the-covid-19-pandemic-on-inflation)
  
### Tool
- Python
    -   [Pandas](https://pandas.pydata.org/docs/): Data Cleaning & Analysis
    -   [Matplotlib](https://matplotlib.org/stable/): Data Visualization
    -   You can use any Python interface to run the code. For beginner recommendation, [Google Colab](https://colab.research.google.com/) is a easy-to-use web based platform to execute Python!

### Exploratory Data Analysis

This EDA explores some key economic concepts and phenomenons using real-life data, including:
- What is the relationship between real and nominal GDP?
- What was the effect of the COVID-19 Pandemic on inflation?
- Does printing money leads to larger inflation? ("Inflation is always and everywhere a monetary phenomenon." (Milton Friedman, 1970))

### Data Sources
This analysis will be using monthly data publicly available at [FRED](https://fred.stlouisfed.org). All data used is available in the [Raw Data folder](https://github.com/kshao19/Money_and_Banking_Analysis/tree/main/Raw%20Data/) in this repository but is last downloaded in 2021. 
- [Real and Nominal GDP](https://github.com/kshao19/Money_and_Banking_Analysis/blob/main/Raw%20Data/Nominal_Real%20GDP.csv)
- [CPI, PPI, PCE](https://github.com/kshao19/Money_and_Banking_Analysis/blob/main/Raw%20Data/part2.csv)
- [Money Supply M1, Money Supply M2](https://github.com/kshao19/Money_and_Banking_Analysis/blob/main/Raw%20Data/Money%20Stock.csv)

### Results and Findings
#### 1. What is the Relationship between Real and Nominal GDP

This analysis seeks to understand the similarities and differences between the real and nominal GDP growth rate. In addition, this analysis seeks to calculate the GDP deflator and understand whether it is a measure of inflation. 
Code to reproduce the analysis is available [here](https://github.com/kshao19/Money_and_Banking_Analysis/blob/main/Code/GDP).

![image](https://github.com/user-attachments/assets/aee3e54a-9b2e-4bbf-ae5d-db183a14dc2e)

The chart plots the year-to-year nominal GDP growth rate along with the real GDP growth rate from 1980 to 2021. I calculate the growth rate as $\frac{GDP_{t} - GDP_{t-1}}{GDP_{t-1}}$. Real and nominal GDP move in similar directions, as both reflect actual changes in national total outputs, i.e. changes in all final goods & services. Nominal GDP growth is always higher than the real GDP. The difference between them is due to changes in the price level (the costs of outputs), which is the inflation.

![image](https://github.com/user-attachments/assets/e1f467a6-32b8-4880-8abc-d0f5124a2885)

GDP Deflator is a measure of the relative difference between the real and nominal GDP. It is a measure of the aggregate price level, showing the level of prices of all final goods and services in an economy at a point of time. Therefore, the change of GDP deflator through time is a measure of inflation, which is used to show the the growth rate of the aggregated price level within a period of time.

#### 2. Effect of the COVID-19 Pandemic on Inflation

This analysis calculates year-to-year inflations using 3 indicators of price level: PPI (Producer Price Index), CPI (Consumer Price Index), PCE (Personal Consumption Expenditures). 
Code to reproduce the analysis is available [here](https://github.com/kshao19/Money_and_Banking_Analysis/blob/main/Code/GDP).

![image](https://github.com/user-attachments/assets/39875d1e-2986-44c0-b215-e2d40f0d0561)

The chart plots the year-to-yeare inflation from 1980 to 2020 using PPI, CPI, and PCE data. Take CPI for example, I calculate the inflation as $100*\frac{CPI_{t} - CPI_{t-1}}{CPI_{t-1}}$.


