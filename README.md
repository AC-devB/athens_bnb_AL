# Athens Airbnb Market Analysis
This project explores the Athens Airbnb market by analyzing data to uncover trends in pricing, demand and customer behavior. The analysis was conducted using SQL and PostgreSQL for database management, cleaning and querying, as well as Power BI to visualize key findings. The goal was to demonstrate skills in database management and extract important insights.

## Tools & Technologies
**PostgreSQL**: Database setup.

**SQL (DBeaver)**: Data import, cleaning and SQL queries.

**Power BI**: Data visualization and dashboard creation.

## [Database Design & SQL Analysis]
Data was sourced from the Inside Airbnb project. A PostgreSQL database was set and raw CSV files were imported. Using SQL, data cleaning was performed to ensure data integrity and usability.

* **Database Setup & Cleaning**: Imported raw Airbnb CSV data into PostgreSQL, removed duplicates, standardized dates and handled missing values.
* **Data Type Conversion**: Cleaned and converted price from text to numeric by stripping symbols/commas.
* **Exploratory Analysis**: Wrote SQL queries to analyze listings, hosts and reviews, discovering trends and patterns in the Athens Airbnb market.

As an example, below is the SQL querry that was used to set up the table schema for storing Airbnb-style listing data.
#### *Creation of schema*

```sql
CREATE TABLE listings (
    id BIGINT PRIMARY KEY,
    name TEXT,
    host_id BIGINT,
    host_name TEXT,
    neighbourhood TEXT,
    latitude DECIMAL,
    longitude DECIMAL,
    room_type TEXT,
    price TEXT,
    minimum_nights INT,
    number_of_reviews INT,
    last_review DATE,
    reviews_per_month NUMERIC,
    calculated_host_listings_count INT,
    availability_365 INT
);
```

## [Power BI Visualization]
An interactive dashboard was created in Power BI to present the key findings in a visually compelling way. The dashboard includes:

* **KPI Cards**: Prominent Key Performance Indicator (KPI) cards were used to display crucial metrics at a glance, such as: Average Price and Total Number of Listings
* **Geographic Map**: A map visualization was used to plot all Airbnb listings across Athens. This allowed for an immediate visual understanding of host density and location-based pricing variations. Users can interact with the map to check out specific neighborhoods.
* **Bar Chart**: A bar chart was created to rank the most popular neighborhoods in Athens by the number of listings. This provides a clear, at-a-glance view of which areas are saturated with Airbnb properties.
* **Pie Chart**: A pie chart was created showcasing the most popular choices among airbnb types such as entire homes or private rooms.

## [Insights]
Below are some of the most important insights of this project:

**Airbnb listings are concentrated in central neighborhoods**: Central Athens has the highest prices and most hosts.

**Entire homes are the most profitable**: They cost more and have higher occupancy than private rooms.

**Reviews increase price**s: Listings with more reviews tend to have higher average prices.

**The market is seasonal**: Demand and prices peak during the summer months.
