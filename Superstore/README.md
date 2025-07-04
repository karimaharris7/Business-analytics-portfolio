# Business Analytics Project: Superstore Profitability Analysis with Tableau
## Project Overview
This project focuses on a comprehensive business analytics initiative aimed at improving the profitability of a struggling superstore. As a consultant, my role involved leveraging Tableau for data visualization to identify key areas of profit and loss, assess advertising effectiveness, and analyze product return rates. The insights derived are crucial for strategic decision-making to prevent the superstore from facing bankruptcy.

## Problem Statement
The superstore is experiencing financial difficulties, and the objective of this project is to provide data-driven recommendations to increase its profitability. This involves answering critical business questions through detailed data visualization and analysis.

## Data Sources
The primary dataset used for this analysis is Superstore.xls, which contains detailed operational data for the superstore. The analysis also incorporates a Returns table, which needs to be joined with the Orders table for return rate analysis.

## Methodology
The project was structured into several main parts, each addressing a specific aspect of the superstore's operations. For each question, an individual visualization was prepared to justify the conclusions.

### Part 1: Profits & Losses
This section aimed to identify the most significant profit centers and loss-makers within the superstore's operations.

Objective: Pinpoint areas contributing most to profit and loss.

Analysis:

- Identified the two biggest profit centers and two biggest loss-makers among various dimension pairs (e.g., subcategory + region, shipping mode + product ID) [cite: superstore.pdf].

- Determined which specific products the superstore should discontinue selling [cite: superstore.pdf].

- Selected three product subcategories to focus on and three to stop selling.

Deliverables: Individual visualizations justifying each conclusion.

### Part 2: Advertising Strategy
This part explored the potential return on investment for advertising efforts, considering temporal and geographical factors.

Objective: Identify optimal advertising opportunities and determine a justifiable advertising spend.

Analysis:

- Identified the 3 best combinations of states and months of the year to advertise in [cite: superstore.pdf].

- Created a visualization showing the average profit for each month of the year for those 3 states [cite: superstore.pdf].

- Argued for the willingness to pay in advertising for these specific state-month combinations, based on a return on ad spend ratio (willing to spend 1/5 of profits on advertising) [cite: superstore.pdf].

Deliverables: Visualizations and a justification for advertising spend.

### Part 3: Returned Items Analysis
This section focused on analyzing product return rates to identify problematic products and customer behaviors.

- Objective: Understand return patterns and their impact on profitability.

- Data Preparation Hint: Ensured the Returns table was LEFT JOINed onto the Orders table, resulting in "Yes" and "null" values in the Returned column.

- Calculated Field: Transformed the Returned field into a calculated field where null values were 0 and Yes values were 1. The average of this field is the return rate, while the total returns are the count or sum of returns [cite: superstore.pdf].

Analysis:

- Identified products with the highest return rates using a visualization [cite: superstore.pdf].

- Identified customers with the highest return rates using a visualization [cite: superstore.pdf].

- Created a separate visualization showing the average profit against the average return rate on a chosen dimension (e.g., state, shipping mode, product type) [cite: superstore.pdf].

- Presented a visual argument for whether the superstore should continue or discontinue business on the basis of this dimension [cite: superstore.pdf].

Deliverables: Multiple visualizations addressing return rates and their impact.

### Part 4: Storytelling with Data (Sprint 5)
This part focuses on a deeper analysis of returned orders to understand their root causes and propose solutions to reduce their volume. The analysis is prepared for the CEO of the Superstore.

Objective: Determine the root causes of high return volumes and recommend strategies for reduction.

Data Preparation:

- Ensured the Returns table is LEFT JOINed onto the Orders table.

- Created a calculated field for Returned where null values are 0 and Yes values are 1. The average of this field represents the return rate, while the count or sum represents total returns.

Worksheet Analysis: At least one worksheet was built for each of the following views on return rates:

- Sales vs. Returns Scatterplot: Showing the correlation between total sales and total returns, aggregated by product subcategory, to assess if sales always correlate positively with returns.

- Return Rate by Product Category: A bar chart visualizing return rates across different product categories.

- Return Rate by Customer: Identifying customers prone to making returns, with a filter to exclude customers with only 1 order.

- Geographic Return Rate Map: A map showing return rates by geographic measure (state, city, etc.) to identify concentrations of returned orders.

- Seasonal Return Rate (Time Series): Analyzing return rates by a measure of time (month, week, etc.) to detect seasonal effects.

- Composite Charts: Two different composite charts illustrating return rates for a mix of multiple factors (date/geography/product category/etc.).

Dashboard Building:

- Created low-fidelity mock-ups (at least 3 variations) and selected a favorite for implementation in Tableau.

- Developed a dashboard template using empty containers to match the chosen mock-up.

- Added the created worksheets to the dashboard template, finalizing with relevant markers, images, and titles.

Presentation & Storytelling:

- Constructed a story arc for the presentation, drafting story points using only captions initially.

The draft story included:

- A summary of the analysis of returns, discussing how returns should be measured (return rate, total cost, or total number) and when each measure is more appropriate.

- Key root causes of returns.

- An overview of each dashboard component, explaining its content and interpretation.

- A demonstration of dashboard usage, including how to interpret it and use filters to identify root causes.

- Proposed actions based on dashboard insights.

- A conclusion with next steps (e.g., dashboard implementation).

- Added content to story points using existing and new worksheets, constructing dashboards as presentation-style slides.

- Saved a completed Tableau Story version.

- Prepared a 3 to 5-minute presentation of the Tableau Story (screen recording or PDF format).

Deliverables: Worksheets, mock-ups, dashboard template, finalized dashboard, Tableau Story, and a presentation.

### Part 5: Power BI App Analysis (Sprint 6)
This section focuses on analyzing the landscape of apps on the Shopify platform using Power BI to identify key success factors.

Objective: Determine key factors contributing to the success of a Shopify app.

- Data Source: The shopify.xlsx dataset, containing public data scraped from the Shopify App Store, including four tables: apps, apps_categories, categories, and reviews.

Deliverables: Each numbered part produced a page in a Power BI report, with each question represented by a visualization. Screenshots of the entire screen were taken for each answered sub-question.

### Part 1: App Landscape (New Power BI sheet: "App Landscape")

- Unique App Count: A KPI Card displaying the unique number of apps (7341 applications were reviewed).

- Review Count Over Time: A Line Chart showing the sum of reviews_count on the Y-axis and lastmod date on the X-axis (not in date hierarchy format). The line graph indicates a decline in reviews [cite: Shopify.pdf].

- Reviews vs. Average Rating Scatterplot: A Scatterplot with reviews_count on the X-axis and average rating on the Y-axis. An annotation (Text Box) provided an interpretation: "The scatterplot graph indicates, of those that completed reviews, they rated the apps high." [cite: Shopify.pdf].

### Part 2: Reviews (New Power BI sheet: "Reviews")

- Helpful Reviews Calculation: Created a new calculated column helpful_reviews in the Reviews table using the DAX expression: rating * (1 + helpful_count).

- Average Helpful Reviews: A Card visual displaying the average value of the new helpful_reviews column (e.g., 5.48) [cite: Shopify.pdf].

Developer Answered Analysis: Created a new calculated column developer_answered in the Reviews table using a DAX expression: 1 (or TRUE) if developer_reply is not blank, else 0 (or FALSE). A scatterplot compared the average rating (Y-axis) by the developer_answered column (X-axis). The chart indicates that developers who completed reviews averaged 4.5, while those who did not averaged 4.8 [cite: Shopify.pdf].

### Part 3: App Reviews (New Power BI sheet: "App Reviews")

- Data Model Relationship: Created a many-to-one relationship between the Reviews table (app_id) and the Apps table (id).

- Sum of Rating by Developer (Potentially Misleading): A bar chart with developer on the X-axis and sum of rating on the Y-axis.

- Average Helpful Review by Developer (More Accurate): A new bar chart with developer on the X-axis and helpful_review average on the Y-axis.

- Most Responsive Developers: A bar chart with developer (from the apps table) and the developer_answered column (created in Part 2.2). A visual-level filter was applied to select only rows where reviews_count is greater than 500.

### Part 6: Final Project: Restaurant Analysis (Sprint 7)
This section outlines the plan for the final project, focusing on a comprehensive analysis of Zomato's restaurant data to highlight popular cuisines, frequently visited restaurants, and revenue drivers.

- Objective: To highlight popular cuisines and frequently visited restaurants, and to prove by showing factual stats on graphs and charts of Zomato's restaurants with the highest revenue, user's preference, and popular cuisines.

- Data Source: Zomato restaurant and order data, including tables for restaurant (City, Cost, Cuisine, Rating, Restaurant ID, Restaurant name, Total Ratings) and orders (Currency, Order date, Restaurant ID, Sales quality, Total sales, User ID).

Research Questions/Hypotheses:

- What cuisine pulls the highest revenue?

- Which cuisine and restaurant has the highest revenue?

- What month and year has generated the highest revenue?

- What cuisine is the user's preference?

- Which cuisine items deliver the most revenue?

- Visualizations to be Used:

- Pie charts for cuisine revenue distribution and user preference.

- Bar charts for number of restaurants by cuisine, restaurants with highest revenue, and user preference by cuisine.

- Line graphs/area charts for revenue by month and year.

- Stacked bar charts for cuisine items delivering the most revenue within restaurants.

Data Preparation:

- Establish relationships between restaurant and orders tables (e.g., using Restaurant ID).

- Ensure data types are appropriate for numerical and date fields.

- Potentially create calculated measures for total sales, revenue per cuisine, etc.

Key Findings & Recommendations (from Zomato project PDF):

- Zomato achieved a total revenue of 964 million INR [cite: Zomato.project.pdf].

- North Indian Chinese cuisine pulls in the most revenue (45M INR), followed by Indian (42M INR), North Indian (34M INR), Chinese (27M INR), Indian Chinese (26M INR), and South Indian (22M INR) [cite: Zomato.project.pdf].

- The highest revenue from a single restaurant (ID 6469) is from North Indian Chinese cuisines (6500 INR) [cite: Zomato.project.pdf].

- January is the highest producing month (97 Million INR), and 2018 is the highest producing year (403 Million INR) [cite: Zomato.project.pdf].

- Users primarily prefer North Indian Chinese cuisines (6.47 users), followed by Indian (6.41 users), Chinese (5.06 users), and North Indian (4.78 users) [cite: Zomato.project.pdf].

- Pizza is the most profitable cuisine item, with Domino's Pizza profiting 5 million INR from pizza sales [cite: Zomato.project.pdf].

### Recommendation: Offer North Indian Chinese cuisines and pizza throughout Zomato's restaurants [cite: Zomato.project.pdf].

### Tools Used: Power BI Desktop (based on the screenshots and context from previous sprints).

### Part 7: Project Submission
The final project submission adhered to specific guidelines for sharing and documentation.

- Submission Format: A ZIP archive containing all project files.

- README.md: Included this README.md file with a link to the published Tableau workbook on Tableau Public.

- File Size: Ensured all included files (including additional files) did not exceed 9 megabytes in total.

### Key Findings & Recommendations
(This section would typically be filled with specific insights and recommendations derived from the Tableau and Power BI visualizations after the analysis is complete. For example:)

- Profit Centers: Identified "Office Supplies - Binders" in the "Central" region as a top profit center, suggesting opportunities for increased focus.

- Loss Makers: Highlighted "Technology - Tables" in the "South" region as a significant loss-maker, indicating a need for re-evaluation or discontinuation.

- Advertising Opportunities: Recommended advertising in "California" during "November" due to high average profit per unit sold, with a suggested ad spend of X% of profits.

- High Return Products: Identified "XYZ Product" as having an abnormally high return rate, suggesting quality control issues or misleading product descriptions.

- Customer Retention: Noted that customers in the "East" region generally have lower return rates, indicating stronger customer satisfaction in that area.

return Causes (Sprint 5): Identified [Specific Root Cause 1, e.g., "seasonal spike in returns during holiday months due to gift purchases"] and [Specific Root Cause 2, e.g., "high return rates for certain electronic accessories due to compatibility issues"].

Recommendations to Reduce Returns (Sprint 5): Proposed [Specific Recommendation 1, e.g., "implementing a clearer return policy for holiday purchases"] and [Specific Recommendation 2, e.g., "enhancing product descriptions and compatibility guides for electronic accessories"].

### Shopify App Insights (Sprint 6):

- The overall trend shows a decline in the number of reviews for Shopify apps over time, despite a high average rating for apps that received reviews.

- Developers who respond to reviews tend to have slightly lower average ratings than those who don't, which could indicate that developers are more likely to respond to negative feedback.

- Key success factors for Shopify apps likely involve consistent developer engagement and a focus on categories with high user satisfaction.

### Zomato Restaurant Insights (Sprint 7):

- North Indian Chinese cuisine is the highest revenue generator and most preferred by users.

- Pizza is the most profitable cuisine item, with Domino's Pizza being a top performer.

- January and the year 2018 showed the highest revenue generation.

Recommendation: Focus on promoting North Indian Chinese cuisines and pizza across Zomato's restaurants to maximize revenue and user satisfaction.

### Tools Used
- Tableau Desktop: For data visualization, dashboard creation, and calculated fields.

- Microsoft Excel (or similar spreadsheet software): For initial data preparation and understanding.

- Power BI Desktop: For data modeling, DAX expressions, and report creation.
