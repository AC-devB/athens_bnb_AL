# Athens Airbnb Market Analysis
A data analysis on the Athens Airbnb market.

## Project Overview

This project explores the Athens Airbnb market by analyzing listings and availability data to uncover trends in pricing, demand, and customer behavior. The analysis was conducted using SQL and PostgreSQL for database management, cleaning, and querying, as well as Power BI to visualize key findings.


This project explores the Athens Airbnb market using SQL and Power BI to analyze listing and availability data and create an interactive dashboard to visualize key findings. The goal was to demonstrate skills in database management and extract insights for hosts, investors, and policymakers. The final step involved creating an interactive dashboard in Power BI to visualize key findings.


This project analyzes the Athens Airbnb market using SQL for data management and Power BI for visualization. It explores listings and availability data to uncover pricing, demand, and customer trends, presented through an interactive dashboard for hosts, investors, and policymakers.

## Tools & Technologies
**PostgreSQL**: Database setup, data cleaning and SQL queries.

**DBeaver**: SQL client for data import and exploration.

**Power BI**: Data visualization and dashboard creation.

## Dataset
Data was sourced from the Inside Airbnb project.

listings.csv: Property details (location, price, reviews, host information).

calendar.csv: Daily availability and pricing data.

Key Steps
1. Database Setup
Created a PostgreSQL database named airbnb_project.

Imported raw CSV files into listings and calendar tables.

2. Data Cleaning with SQL
Converted the price field from a text format to a numeric data type by removing currency symbols.

Standardized date formats within the calendar table.

Handled missing values and removed duplicate entries to ensure data integrity.

3. Exploratory Data Analysis (EDA)
Analyzed the average price per neighborhood and room type.

Calculated occupancy rates to identify demand patterns.

Examined the relationship between review count and pricing.

Identified seasonal trends in pricing and availability.

Key Insights
Central Athens neighborhoods have the highest average prices and host density.

Entire homes/apartments are significantly more expensive than private or shared rooms and show stronger occupancy.

Listings with more reviews tend to have higher average prices, highlighting the value of a good reputation.

The Athens Airbnb market shows clear seasonal patterns, with summer months driving increased demand and higher prices.

## [Power BI Visualization]
An interactive dashboard was created in Power BI to present the key findings in a visually compelling way. The dashboard includes:

KPI Cards: Prominent Key Performance Indicator (KPI) cards were used to display crucial metrics at a glance, such as: Average Price and Total Number of Listings

Geographic Map: A map visualization was used to plot all Airbnb listings across Athens. This allowed for an immediate visual understanding of host density and location-based pricing variations. Users can interact with the map to check out specific neighborhoods.

Bar Chart: A bar chart was created to rank the most popular neighborhoods in Athens by the number of listings. This provides a clear, at-a-glance view of which areas are saturated with Airbnb properties.
