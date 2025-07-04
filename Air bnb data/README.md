# BI Analytics Project: Manhattan Airbnb Market Analysis
## Project Overview
This project focuses on analyzing the Manhattan vacation rental market using Airbnb data to provide insights and recommendations on optimal property types for investment. The analysis was conducted as part of "Sprint 1: Spreadsheet Data Analysis" and involved comprehensive data cleaning, pivot table creation, and revenue estimation to identify attractive neighborhoods and popular property sizes.

## Problem Statement
A client sought guidance on which property types to invest in within the Manhattan vacation rental market. The primary objective was to answer two key questions:

- Which neighborhoods and property sizes are most attractive for vacation rentals?

- How much money did these attractive listings generate?

## Data Source
The project utilized NYC Airbnb Data, specifically focusing on listings and calendar information.

## Methodology
The analysis involved several steps using spreadsheet tools to derive actionable insights:

### 1. Data Cleaning
- Neighborhood Cleaning: The 'neighborhood' column labels were cleaned by removing inconsistent capitalization and trailing spaces. Cleaned values were stored in a new column called neighborhood_clean.

- Bedrooms Cleaning: Empty cells in the 'bedrooms' column, representing studio apartments (zero bedrooms), were cleaned and stored in a new column called bedrooms_clean.

### 2. Neighborhood Attractiveness Analysis
- Attractiveness was assessed by analyzing the number_of_reviews_ltm (reviews in the last 12 months).

- A pivot table was created to identify the top 10 most attractive neighborhoods.

- Top 3 Most Attractive Neighborhoods: Lower East Side, Hells Kitchen, and Harlem.

### 3. Property Size Popularity Analysis
- A pivot table was built to determine the most popular property sizes.

- Top 3 Most Popular Property Sizes: Studios (441 listings), 1-bedrooms (1,265 listings), and 2-bedrooms (526 listings).

### 4. Neighborhood-Specific Property Preferences
- The pivot table was updated to recommend specific property sizes for each of the top 10 neighborhoods.

- Harlem Preference: 1-bedroom apartments were found to be the most popular in Harlem.

- General Preference: For most top neighborhoods, 1-bedroom listings were optimal, with the exception of Midtown, where studios were most popular.

- A new column, top_listing, was added to identify listings matching these criteria (1-bedroom in top neighborhoods, or studio in Midtown).

### 5. Revenue Generation Analysis
Revenue Calculation (revenue_earned):

- In the calendar data, revenue_earned was calculated for each night: if available was "f" (rented), revenue_earned was set to adjusted_price; otherwise, it was $0.

- In the listings data, a new revenue_earned column was created using SUMIF() to sum the total revenue_earned from the 30-day calendar data.

- Top-Earning Listing: A pivot table was used to order top listings by revenue, filtered by top_listing.

- The top-earning listing ID was identified as 49946551.

- This listing earned $29,940 over a 30-day period.

- Annual Revenue Estimation: Annual revenue was estimated by multiplying the 30-day total by 12. The top-earning listing (ID 49946551) had an estimated annual revenue of $359,280.

## Key Findings & Recommendations
- The most attractive neighborhoods for vacation rentals in Manhattan are Lower East Side, Hells Kitchen, and Harlem.

- The most popular property sizes are studios, 1-bedrooms, and 2-bedrooms.

- Property size preferences vary by neighborhood, with 1-bedrooms being most popular in Harlem, and studios being most popular in Midtown.

- The top-earning listing (ID 49946551) demonstrated significant revenue potential, earning $29,940 in 30 days, with an estimated annual revenue of $359,280.

- These findings provide a data-driven basis for clients to make informed investment decisions in the Manhattan vacation rental market.

## Tools Used
- Spreadsheet Software (e.g., Microsoft Excel, Google Sheets) for data analysis, pivot tables, and data cleaning functions (e.g., IF, SUMIF).

## Project Deliverables & Best Practices Checklist
The project followed best practices for spreadsheet analysis and documentation:

- Unnecessary columns were hidden.

- The analysis includes an executive summary and a table of contents.

- Data cleaning steps are documented in a change log.

- Assumptions are clearly documented.

- Formatting, borders, cell background colors, font styles, and sizes are consistent across the analysis.
