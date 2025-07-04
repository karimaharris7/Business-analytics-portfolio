# Business Analytics Project: E-commerce User Behavior & Retention
## Project Overview
1 This project focuses on analyzing raw transaction logs from an e-commerce company to derive key business metrics related to user conversion and retention. As a junior analyst, my task was to transform event-level data into actionable insights, providing the executive team with a clearer understanding of user interaction and loyalty on the website.

## Problem Statement
The executive team at an e-commerce company needed a deeper understanding of user behavior on their website. Specifically, they aimed to:

- Understand Conversion Efficiency: How effectively are product page views converting into purchases?

- Analyze User Retention: How do user cohorts behave over time, and what are their retention rates?

## Data Source
### The analysis utilized a dataset named "raw_user_activity," containing event logs of user interactions on the company's website. Each row represents a distinct activity or event.

Dataset Columns:

- user_id: Unique customer identifiers.

- event_type: The type of activity by the user (e.g., 'view', 'shopping_cart', 'purchase').

- category_code: Category of the product (e.g., 'electronics.telephone').

- brand: Company that manufactures the product.

- price: Price of the product in USD.

- event_date: Date of the user activity in YYYY-MM-DD format.

## Methodology
The project was structured into several parts, leveraging advanced spreadsheet techniques for data preparation and analysis.

## Part 1: Build a Conversion Funnel
To visualize how users progress from viewing products to making purchases, a conversion funnel was constructed.

Objective: Understand the conversion rates from product page views to purchases.

Process:

- A pivot table was created on a new sheet named "conversion_funnel" using data from "raw_user_activity."

- Unique users were counted for each of the three funnel stages: 'view', 'shopping_cart', and 'purchase' [cite: Ecommerce.pdf].

- Formulas were used to calculate both total conversion rates (from the initial view stage) and conversion rates to the next step (stage-to-stage conversion) [cite: Ecommerce.pdf].

## Key Findings (Conversion Funnel):

- Of all viewers, 34% placed items in their shopping cart [cite: Ecommerce.pdf].

- 19% of items placed in shopping carts were ultimately purchased [cite: Ecommerce.pdf].

- Overall, the website achieved a 19% purchase conversion rate from initial views [cite: Ecommerce.pdf].

## Part 2: Prepare Data for Cohort Analysis
This section involved extensive data preparation to enable a robust cohort analysis based on users' first purchase months.

### Filter Purchases:

A new sheet, "purchase_activity," was created to isolate only 'purchase' event types from the "raw_user_activity" sheet. This resulted in 4,845 rows of purchase data [cite: Ecommerce.pdf].

### Calculate First Purchase Dates:

- A pivot table on a new sheet, "first_purchase," was used to determine the minimum event_date (first purchase date) for each unique user_id [cite: Ecommerce.pdf].

- The VLOOKUP() function was then used in the "purchase_activity" sheet to populate a new column, first_purchase_date, corresponding to each user_id's first purchase [cite: Ecommerce.pdf].

### Set Up Monthly Data for Cohorts:

- Three new columns were added to the "purchase_activity" sheet:

- event_month: Extracted the month and year (YYYY-MM format) from event_date using the TEXT() function [cite: Ecommerce.pdf].

- first_purchase_month: Extracted the month and year (YYYY-MM format) from first_purchase_date using the TEXT() function [cite: Ecommerce.pdf].

- cohort_age: Calculated the number of months between first_purchase_date and event_date using the DATEDIF() function, ranging from 0 to 4 months [cite: Ecommerce.pdf].

## Part 3: Calculate Retention Rates
The prepared data was then aggregated into cohorts to calculate and track retention rates.

### Group Data into Cohorts:

- A pivot table on a new sheet, "cohort_analysis," was configured.

- Rows represented cohorts based on first_purchase_month (resulting in 6 cohorts) [cite: Ecommerce.pdf].

- Columns represented cohort_age, displaying the count of unique users for each cohort age [cite: Ecommerce.pdf].

### Calculate Overall Retention Rates:

- A blank sheet, "retention_rates," was created to present the retention rates.

- Row labels were added for each cohort (e.g., "2020-09", "2020-10") and column labels for cohort_age from 1 to 4 months (excluding age 0 as it's the acquisition month) [cite: Ecommerce.pdf].

- Formulas were used to calculate the retention rate for each cohort at each cohort_age, based on the starting cohort sizes [cite: Ecommerce.pdf].

### Key Findings (Retention Rates):

- Purchasing users in September 2020 exhibited the highest retention rate of 3.13% at cohort age 4 [cite: Ecommerce.pdf].

- Generally, user activity remained higher during the first 3 months of a cohort's lifecycle [cite: Ecommerce.pdf].

## Part 4: Organize and Document Spreadsheet
To ensure the project was professional and easy to understand, best practices for spreadsheet organization and documentation were applied.

# Executive Summary:

- A "Executive Summary" sheet was populated with a synopsis of the results from the "conversion_funnel" and "retention_rates" sheets [cite: Ecommerce.pdf].

- Detailed explanations were provided on the raw data (timespan, event types, collection method, used parts), the data used for conversion rate calculations (unique user counts), and the methodology for cohort analysis (cohort formation, tracking period, retention rate calculation) [cite: Ecommerce.pdf].

# Sheet Reordering:

- Sheet tabs were reordered for logical flow: "Table of Contents," "Executive Summary," analytical results sheets ("conversion_funnel," "cohort_analysis," "retention_rates"), calculation sheets ("purchase_activity," "first_purchase"), and finally raw data sheets ("raw_user_activity") [cite: Ecommerce.pdf].

# Formatting:

- Numbers and dates were consistently formatted.

- Borders were added to tables.

- Column headers were bolded.

- Rows were frozen for easy navigation.

- Cells containing calculations were highlighted for clarity.

# Conclusion
This project successfully transformed raw e-commerce event logs into meaningful business intelligence. The conversion funnel provides a clear picture of user drop-off points, while the cohort analysis offers valuable insights into user retention over time. These metrics are crucial for the executive team to identify areas for improvement in the user journey and to strategize for enhanced customer loyalty and revenue growth.
