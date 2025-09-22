# Mobile-Sales-Analysis

## Overview:
__This is a Sales Report for Mobile Sales Products__

---

## Contents
Project Overview | Data Source | Tools Used | Table Outlay | Query Language (SQL) | Visualisation 

---

## Project Overview:
> > This Project Analyzes the sales of Mobile Sales Products to uncover insights on sales distribution by various attributes as Brands, Customer Gender and Payment Methods , using pivot tables, I explore Metrics like total sales by Payment Methods and Gender, average income of buyers, gender distribution, and overall revenue. This analysis helps to understand the key factors driving sales in the dataset provided.
`
## Data Source:
www.Kaggle.com/dataset 

## Tools Used:
+ Pivot Table / Charts 
+ PowerBI
+ SQL

## Table Outlay:
First Three Records

|TransactionID	|Date	|MobileModel	|Brand	|Price	|UnitsSold	|TotalRevenue	|CustomerAge|	CustomerGender |	Location |	PaymentMethod|
|---------|--------|--------|----------|----------|---------|---------|----------|------------|--------|---------|
|79397f68-61ed-4ea8-bcb2-f918d4e6c05b	|1/6/2024	|direction	|Green Inc|	1196.95| 85	|28002.8	|32	|Female| Port Erik	|Online|
|4f87d114-f522-4ead-93e3-f336402df6aa	|4/5/2024	|right	|Thomas-Thompson|	1010.34|	64	|2378.82	|55	|Female| East Linda|	Credit Card|
|6750b7d6-dcc5-48c5-a76a-b6fc9d540fe1	|2/13/2024	|summer	|Sanchez-Williams|	400.8|	95|	31322.56|	57	|Male	|East Angelicastad|	Online|

## Query Language (SQL) 
Some of the query languages to retrieve records are displayed here 

```SQL
---1.CATEGORIZE THE DATA INOT GOLD,SILVER AND DIAMOND
SELECT *,
CASE
WHEN PRICE < 500 THEN 'silver'
WHEN PRICE BETWEEN 500 AND 999 THEN 'gold'
ELSE 'diamond'
END AS category
FROM mobile_sales;

---2.RETRIEVE ALL FEMALE CUSTOMERS THAT BOUGHT GOODS ABOVE 900---
SELECT * FROM mobile_sales
WHERE customergender = 'female'
AND price >900;

---3.RETRIEVE THE SALES BY PAYMENT METHOD ARRANGING FROM LARGEST TO SMALLEST AMOUNT---
SELECT * FROM mobile_sales
ORDER BY paymentMethod;

```

## Visualization
### Pivot Table 







