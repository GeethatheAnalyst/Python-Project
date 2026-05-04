# E-Commerce Business Analysis — Python

I was given the role of a business analyst for an e-commerce company and asked to prepare a report on the data. This project covers the full EDA process — from loading and cleaning the data, to summarising it at different levels, to calculating actual revenue figures.
---

## What the project covers

**Data familiarisation**
First looked at the shape, data types, null values, and structure of the dataset. Found that 3 date columns (Order Date, Expected Delivery Date, Delivered Date) were stored as objects and needed to be converted to datetime format before any time-based analysis.


**Cleaning**
Dropped two non-informative columns (`product_specifications` and `description`) that added noise without useful signal. Also stripped whitespace from the Brand column — caught a dirty data issue where "Tarkan" had a trailing space that was creating a duplicate brand entry.

**Brand-level analysis**
Found the number of unique brands and calculated average product ratings per brand. 

**Category analysis**
Visualised the count of orders per product main category using a bar chart. Identified which categories had the highest and lowest order volumes, and pulled the top 5.

**Revenue calculation**
This was the most business-relevant part. The company uses a tiered commission structure:
- 25% on orders with discounted price > 600
- 15% on orders between 351–600
- 10% on orders between 101–350
- 0% on orders ≤ 100

Calculated e-commerce platform revenue for every order using this logic, then found total platform revenue by summing across all orders.

**Brand revenue**
Calculated brand-level revenue (what each brand actually earns after the platform takes its cut) and listed the top 10 brands by revenue in descending order.

**Price analysis**
Drew boxplots comparing retail price vs discounted price — found outliers in both. Created a scatterplot of retail price vs discounted price to visualise the discount relationship across products.

---

## Tools used

- Python 3
- Pandas (data manipulation and groupby)
- Matplotlib (bar charts, boxplots, scatter plots)
- Seaborn
- Jupyter Notebook

---

## Dataset

E-commerce sales dataset provided as part of coursework at RRC Technologies, Thanjavur.
