# London-Housing-Data-Analysis

## Overview
This project provides a comprehensive analysis of the London Housing Dataset spanning from 1995 to 2019. The dataset offers valuable insights into the London housing market, including average house prices, number of houses sold, and crime statistics across different areas. The goal of this project was to identify key trends, uncover housing market dynamics, and explore the relationship between house prices and crime rates over time.

## Key Objectives
Analyze the trends in average house prices across various regions in London.
Investigate crime statistics in relation to housing prices.
Extract insights to assist in data-driven decision making for real estate investments or policy planning.
Tools & Technologies Used
Python: For data analysis and manipulation.
Pandas: To clean, preprocess, and analyze the dataset.
Matplotlib & Seaborn: For data visualization and insightful graphical representations.
Jupyter Notebook: Development environment to execute the analysis.

## Dataset
The dataset includes:

Date: Transaction date (from 1995 to 2019)
Average price: The average house price for each region.
Number of houses sold: Total houses sold in a given time frame.
Crime statistics: Number of crimes reported in various regions.
Steps in the Analysis
1. Data Preparation
Converted the 'Date' column to DateTime format for time-based analysis.
Created new columns for Year and Month to facilitate temporal insights.
2. Data Cleaning
Removed unnecessary columns to streamline the dataset.
Handled missing values and detected outliers to ensure data quality.
3. Exploratory Data Analysis (EDA)
Crimes: Identified and quantified records with zero crimes reported.
Average House Prices: Analyzed maximum and minimum house prices per year in different regions of England.
Crime Rates: Explored the maximum and minimum number of crimes recorded per area.
Price Segmentation: Counted records for areas where average prices were below £100,000.
## Key Insights

House Prices Trends:

The analysis revealed significant growth in average house prices in London from 1995 to 2019.
Certain regions showed consistently higher prices, indicating more desirable areas for living or investment.

Crime Statistics:

Regions with higher house prices typically had lower crime rates.
Areas with zero crimes reported were identified, suggesting safer neighborhoods.

Low-Priced Areas:

A notable number of records showed average house prices below £100,000, mostly concentrated in certain areas, providing opportunities for affordable housing investment.
Python Code Highlights

## Data Manipulation:
pd.to_datetime() was used to convert date columns into the correct format.
New columns were created to extract Year and Month from the Date column.
Unnecessary columns were dropped using df.drop() to keep the dataset relevant.

## Exploratory Data Analysis:
GroupBy techniques were used to aggregate data for better insights, such as:
python
Copy code
df.groupby('Year')['Average_Price'].mean()

## Visualization:
Seaborn and Matplotlib were used for visualizations like heatmaps and line plots to reveal trends in housing prices and crime statistics.

## Example:
python
Copy code
sns.heatmap(df.isnull(), cmap="coolwarm")
Sample Queries Solved
Convert Date Column:
pd.to_datetime(df['Date'])
Add Year & Month Columns:
df['Year'] = df['Date'].dt.year
df['Month'] = df['Date'].dt.month
Filter for Zero Crimes:
df[df['No_of_Crimes'] == 0]

## Conclusion
Through this analysis, I gained a deeper understanding of the London housing market's key drivers, particularly how crime rates and housing prices correlate over time. The project provided valuable experience in handling real-world datasets, employing advanced data manipulation techniques using Python, and generating meaningful insights to support data-driven decision making.
