# Real-Estate-Analysis-Project

## Overview
The overarching goal of this project is to use post-pandemic real estate sales data to illustrate market trends. 

## Data
Data on over 150,000 residential home sales were exported from the Triangle MLS to be used for this analysis. Data fields included the following: MLS#, Class, Propety Type, Address, City, Zip Code, Neighborhood, Subdivision, Bedrooms, Baths, Square Footage, Acreage, Year Built, List Date, Closing Date, Days on Market, List Price, and Sold Price. Data was engineered as needed, such as ensuring that we only examine trends for comparable properties. Superfluous columns with high NaN occurances were dropped, such as "Neighborhood" and "Subdivision". Acreage was listed as a given range if the property's actual acreage fell within that range, and the acreage was replaced by the mean value of that range (i.e., if the range was 1-2 acres, the value would be replaced with 1.5 acres). For certain questions, all cities that contained less than 10 total data points/sales were dropped, as many are not typically included in the Triangle MLS market and so this data could skew results.

## Scope
The scope of this project is to use python visualizations, and rudimentary machine learning through the time-series model "Prophet", to answer questions about Triangle NC real estate market trends in general, and to make predictions for a specificallly-defined subset of homes. The general market questions are as follows:
1. How does seasonality affect the volume of home sales?
1. How does seasonality affect the amount that individuals are paying over asking price (both as an absolute value and as a percentage of list price)?
1. How do mortgage rates affect the volume of home sales?
1. How do mortgage rates affect the difference between list price and sold price?

Specific questions were answered which focused on comparable homes in the Raleigh area, with their criteria being, single-family detached homes, 3 beds, 2 baths, xxx square feet plus or minus 10%, xxxx acres:
1. Are we able to make a prediction for days on market based on list date?
2. Are we able to make a prediction for how far above list price someone should offer based on list date?
3. Are we able to make a prediction for days on market based on mortgage rates?
4. Are we able to make a prediction for how far above list price someone should offer based on mortgage rates?
    
## Results