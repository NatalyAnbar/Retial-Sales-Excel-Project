# Sales Data Analysis
## Project Overview
This project analyzes a real‑world sales dataset containing 65,507 transactions. The goal was to transform a raw, unstructured Excel file into a clean, reliable, and analytics‑ready model, then extract meaningful business insights using Power Query, Power Pivot, DAX, and an Excel dashboard.

The project demonstrates practical skills in data cleaning, normalization, data modeling, and business analytics.
## Dataset Structure
The original dataset was delivered as one flat table containing orders, customer information, and product details.
To improve structure and reduce redundancy, the data was normalized into a 3‑table Star Schema:

Orders (Fact Table) – All sales transactions

Customers (Dimension Table) – Unique Customer IDs and Countries

Products (Dimension Table) – Unique Product IDs and Descriptions

The Customers and Products tables were created by extracting unique IDs and retrieving attributes using XLOOKUP.
## Data Cleaning Summary

A series of cleaning steps were applied to ensure data quality:

Invalid Descriptions: Fixed ~2% invalid product descriptions using Fill‑Down after verifying ProductID consistency.

Quantity Issues: Removed negative values (<1%) and three extreme outliers (>15,000 units).

Unit Price Outliers: Removed zero and extremely high prices (~0.2%).

Missing Customer IDs: ~25% were missing; kept and labeled as "Unknown" to avoid major data loss.

These steps ensured the dataset was consistent, accurate, and ready for modeling.

## DAX Mesaures

Several business metrics were created to support analysis:

Amount (calculated column): Unit Price × Quantity

Average Order Value (AOV)

Avg Orders Per Customer

Avg Revenue Per Customer

Avg Revenue Per Product

Quantity Per Order

Product Ranking (Quantity & Revenue) using RANKX

These measures enabled deeper insights into customer behavior and product performance.

## Key Insights
Peak Sales Hours: Most transactions occur between 12:00 PM and 3:00 PM.

Top Product by Quantity: White Hanging Heart T‑Light Holder.

Top Product by Revenue: 3 Tier Cake Stand (driven by high price).

Geographical Trends:

UK dominates with 90% of customers and 86% of revenue.

New Zealand and Japan show much higher AOV than the UK.

## Strategic Recommendations
Increase inventory for high‑volume items.

Target high‑value markets (New Zealand, Japan).

Collect product cost data to enable profit analysis.

Schedule promotions around peak shopping hours.

## Full Report
For detailed cleaning steps, DAX formulas, and full business analysis, see the full report:



