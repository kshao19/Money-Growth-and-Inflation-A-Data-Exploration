# Money Growth and Inflation: A Data Exploration
## This is an analysis that proves and visualizes macroeconomic theories for Money &amp; Banking

## Table of Contents
- [Tool](#tool)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Sources](#data-sources)
- [Results and Findings](#results-and-findings)
  - [1. What is the relationship between real and nominal GDP](#1-what-is-the-relationship-between-real-and-nominal-gdp)
  - [2. Effect of the COVID-19 Pandemic on Inflation](#2-effect-of-the-covid-19-pandemic-on-inflation)
  - [3. Inflation and Money Growth](#3-inflation-and-money-growth)
  - [4. Examine Portfolio Choice Theory](#4-examine-portfolio-choice-theory)
  
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
- Does consumer data support Portfolio Choice Theory?

### Data Sources
This analysis will be using monthly data publicly available at [FRED](https://fred.stlouisfed.org) and [Survey of Consumer Finance (SCF)](https://www.federalreserve.gov/econres/scfindex.htm). All data used is available in the [Raw Data folder](https://github.com/kshao19/Money_and_Banking_Analysis/tree/main/Raw%20Data/) in this repository but is last downloaded in 2021. 
- [Real and Nominal GDP](https://github.com/kshao19/Money_and_Banking_Analysis/blob/main/Raw%20Data/Nominal_Real%20GDP.csv)
- [CPI, PPI, PCE](https://github.com/kshao19/Money_and_Banking_Analysis/blob/main/Raw%20Data/part2.csv)
- [Money Supply M1, Money Supply M2](https://github.com/kshao19/Money_and_Banking_Analysis/blob/main/Raw%20Data/Money%20Stock.csv)
- [2019 SCF](https://github.com/kshao19/Money_and_Banking_Analysis/blob/main/Raw%20Data/sub-data.zip)

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

During the COVID 19, due to decreasing consumer demand and physical limitations in production and consumption, inflation dropped. Inflation measured by CPI dropped the least, followed by PPI, and inflation measured by PCE dropped the most. Given the definitions for PPI, CPI, and PCE, we see that the short-term impact of the pandemic is on government restriction on consumers to access goods and services, which decreased consumer demand severely.

- CPI is fixed upon a constant quantity of goods and services. Thus, only price changes will lead to changes in the CPI.
- Similarly, PPI measures the average movement in the costs of a fixed quantity of domestic production.
- PCE takes into account the total value of personal consumption expenditures every month. In the mid of COVID and facing uncertainty and health concerns, consumers might be reluctant to purchase a lot of non-essential goods and services. Thus the quantity reduction will be reflected in the growth rate of PCE.

#### 3. Inflation and Money Growth

Milton Friedman once wrote that "Inflation is always and everywhere a monetary phenomenon."  This analysis seeks to compare inflation (as measured by CPI) and growth rate in M1 and M2 money supply. M1 money supply consists of physical currency and coin, demand deposits, traveler's checks, and other checkable deposits. M2 money supply consists of all components of M1 plus several less-liquid assets such as savings deposit. Code to reproduce the analysis is available [here](https://github.com/kshao19/Money_and_Banking_Analysis/blob/main/Code/Money%20Growth).

The chart plots the year-to-yeare inflation and money growth from 1960 to 2020. Inflation is calculated using the same methodology as #2. Money growth is calculated as $100*\frac{M_{t} - M_{t-1}}{M_{t-1}}$.

![image](https://github.com/user-attachments/assets/4b2538f4-0b8f-4c3f-b693-4f88b9911a3a)
![image](https://github.com/user-attachments/assets/d32f427d-cbba-4557-a6a4-8f723c515575)
![image](https://github.com/user-attachments/assets/76507d51-45ce-458c-a709-64e1cec3deb5)

- During 1960-1980, inflation has a mostly positive relationship with money growth (both M1 & M2), an increase in money growth is followed immediately or shortly by an increase in inflation, which seems to prove the phrase "Inflation is always and everywhere a monetary phenomenon."
- During 1981-1990, changes in the inflation appears to lag the changes in M1 and M2.
- From 1991-2009, changes in the inflation appears to lag the changes in M1 and M2. From 2010 - 2020, inflation is moving in the same direction as M1 and M2.

From the plotting, it is difficult to conclude whether inflation will always follow money growth.

#### 4. Examine Portfolio Choice Theory

This analysis uses the 2019 result of Survey of Consumer Finance (SCF) which records data on U.S. household balance sheets, pensions, income, and demographic characteristics. Code to reproduce the analysis is available [here](https://github.com/kshao19/Money_and_Banking_Analysis/blob/main/Code/Portfolio%20Choice%20Theory).

Portfolio Choice Theory assumes that as wealth increases, investors have more resources to purchase assets, therefore, their demand for money increases. In addition, the more income household have, Portfolio Choice Theory assumes that their ability to hold a variaty of assets increases, including their ability to hold money, given a cateris paribus assumption to accumulate wealth. The left chart shows the relationship between asset and avergae liquid holding by income decile groups. The right chart shows the relationship between income and avergae liquid holding by asset decile groups.

- For any income level, the more asset a household has, the more liquid asset it will hold, which supports the Portfolio Choice Theory. 
- Generally, for any wealth level, the more income they have, their liquid asset holding increases. This is consistent with the prediction of Portfolio Choice Theory.
  - However, for people who have the most wealth, i.e. those in the 9th-10th asset decile groups, although the overall trend increases, those people who have the medium level of income actually have the lowest amount of liquid asset holding.
  
![image](https://github.com/user-attachments/assets/d842a45c-1a27-4876-b0c9-beb3e22c52b7)

Portfolio Choice Theory assumes that people choose a variety of assets according to their relative return, risks, liquidity, as well as people's own wealth and income. The left plot shows the relationship between asset and share of liquid holding by income decile groups. The right chart shows the relationship between income and share of liquid holding by asset decile groups. 
- Increasing asset is correlated to decreasing trend in the share of liquid asset, which supports the Portfolio Choice Theory. It shows that as people have more wealth, they are less likely to put all the asset into cash. They will care more about the relative expected return and the risks of the asset than the relative liquidity of the asset. Although liquid asset is easier to be cashed out, it does not generate more return as other assets such as bonds, equities, or goods or services like a car.
-  For people who has lower wealth and lower income, liquidity matters more. As those people get more income, they would still want to hold cash so that they can use it, and they are more likely to use it at any time. But for people who has a higher wealth, as they have more income, they might only want to hold a certain level of cash and use the increasing income to invest in other assets because they already have a high wealth.

![image](https://github.com/user-attachments/assets/c665369e-16e3-4f00-a21c-30bfdd7d73ac)






