# Athens Airbnb Market Analysis
This project explores the Athens Airbnb market by analyzing data to uncover trends in pricing, demand and customer behavior. The analysis was conducted using SQL and PostgreSQL for database management, cleaning and querying, as well as Power BI to visualize key findings.

## Tools & Technologies
**PostgreSQL**: Database setup.

**SQL (DBeaver)**: Data import, cleaning and SQL queries.

**Power BI**: Data visualization and dashboard creation.

## Visual Graph examples

### ***Main graph***
<img width="1459" height="819" alt="athens_BI_main" src="https://github.com/user-attachments/assets/c0903774-fb60-422b-9c94-177027592b03" />

### ***Graph sorted by Private rooms available***
<img width="1457" height="819" alt="athens_BI_room" src="https://github.com/user-attachments/assets/3f9c6d8e-5514-4a71-84e6-c064ae5b7784" />

### ***Map of available Airbnb listings in Athens***
<img width="1479" height="841" alt="athens_BI_map2" src="https://github.com/user-attachments/assets/c145b4ef-f426-416f-bae2-7373a0eb4849" />


## [Database Design & SQL Analysis]
Data was sourced from the Inside Airbnb project. A PostgreSQL database was set and raw CSV files were imported. Using SQL, data cleaning was performed to ensure data integrity and usability.

* **Database Setup & Cleaning**: Imported raw Airbnb CSV data into PostgreSQL, removed duplicates, standardized dates and handled missing values.
* **Data Type Conversion**: Cleaned and converted price from text to numeric by stripping symbols/commas.
* **Exploratory Analysis**: Wrote SQL queries to analyze listings, hosts and reviews, discovering trends and patterns in the Athens Airbnb market.

As an example, below is the SQL query that was used to set up the table schema for storing Airbnb-style listing data, along with a query that finds the top 20 hosts with the most listings in the dataset.
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
#### *Top 20 hosts in Athens with the highest number of Airbnb listings*

```sql
SELECT
    host_id,
    host_name,
    COUNT(*) AS total_listings
FROM listings
GROUP BY host_id, host_name
ORDER BY total_listings DESC
LIMIT 20;
```


## [Power BI Visualization]
An interactive dashboard was created in Power BI to present the key findings in a visually compelling way. The dashboard includes:

* **Cards**: Key metrics are presented like average price and total listings.
* **Geographic Map**: An interactive map of Athens listings, showing host density and pricing by neighborhood.
* **Bar Chart**: Neighborhoods were ranked by number of listings to show the most popular areas.
* **Pie Chart**: Distribution of Airbnb types was displayed such as entire homes versus private rooms.

## [Insights]
The goal of this project was to demonstrate skills in database management and extract important insights. Below are some of these insights:

* **Airbnb listings are concentrated in central neighborhoods**: Central Athens has the highest prices and most hosts.
* **Entire homes are the most profitable**: They cost more and have higher occupancy than private rooms.
* **Reviews increase price**s: Listings with more reviews tend to have higher average prices.
* **The market is seasonal**: Demand and prices peak during the summer months.
