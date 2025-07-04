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

- Identified the two biggest profit centers and two biggest loss-makers among various dimension pairs (e.g., subcategory + region, shipping mode + product ID).

- Determined which specific products the superstore should discontinue selling.

- Selected three product subcategories to focus on and three to stop selling.

- Deliverables: Individual visualizations justifying each conclusion.

### Part 2: Advertising Strategy
This part explored the potential return on investment for advertising efforts, considering temporal and geographical factors.

Objective: Identify optimal advertising opportunities and determine a justifiable advertising spend.

Analysis:

- Identified the 3 best combinations of states and months of the year for advertising.

- Created a visualization showing the average profit for each month of the year for these three states.

- Argued for the willingness to pay in advertising for these specific state-month combinations, based on a return on ad spend ratio (willing to spend 1/5 of profits on advertising).

- Deliverables: Visualizations and a justification for advertising spend.

### Part 3: Returned Items Analysis
This section focused on analyzing product return rates to identify problematic products and customer behaviors.

Objective: Understand return patterns and their impact on profitability.

Data Preparation Hint: Ensured the Returns table was LEFT JOINed onto the Orders table, resulting in "Yes" and "null" values in the Returned column.

Calculated Field: Transformed the Returned field into a calculated field where null values were 0 and Yes values were 1.

Analysis:

- Identified products with the highest return rates using a visualization.

- Identified customers with the highest return rates using a visualization.

- Created a separate visualization showing the average profit against the average return rate on a chosen dimension (e.g., state, shipping mode, product type).

- Presented a visual argument for whether the superstore should continue or discontinue business based on this dimension.

- Deliverables: Multiple visualizations addressing return rates and their impact.

### Part 4: Storytelling with Data (Sprint 5)
This part focuses on a deeper analysis of returned orders to understand their root causes and propose solutions to reduce their volume. The analysis is prepared for the CEO of the Superstore.

Objective: Determine the root causes of high return volumes and recommend strategies for reduction.

Data Preparation:

- Ensured the Returns table is LEFT JOINed onto the Orders table.

- Created a calculated field for Returned where null values are 0 and Yes values are 1. The average of this field represents the return rate, while the count or sum represents total returns.

- Worksheet Analysis: At least one worksheet was built for each of the following views on return rates:

- Sales vs. Returns Scatterplot: Showing the correlation between total sales and total returns, aggregated by product subcategory, to assess if sales always correlate positively with returns.

- Return Rate by Product Category: A bar chart visualizing return rates across different product categories.

- Return Rate by Customer: Identifying customers prone to making returns, with a filter to exclude customers with only 1 order.

- Geographic Return Rate Map: A map showing return rates by geographic measure (state, city, etc.) to identify concentrations of returned orders.

- Seasonal Return Rate (Time Series): Analyzing return rates by a measure of time (month, week, etc.) to detect seasonal effects.

Composite Charts: Two different composite charts illustrating return rates for a mix of multiple factors (date/geography/product category/etc.).

Dashboard Building:

- Created low-fidelity mock-ups (at least 3 variations) and selected a favorite for implementation in Tableau.

- Developed a dashboard template using empty containers to match the chosen mock-up.

- Added the created worksheets to the dashboard template, finalizing with relevant markers, images, and titles.

Presentation & Storytelling:

- Constructed a story arc for the presentation, drafting story points using only captions initially.

The draft story included:

- A summary of the analysis of returns, discussing how returns should be measured (return rate, total cost, or total number) and when each measure is more appropriate.

Key root causes of returns.

- An overview of each dashboard component, explaining its content and interpretation.

- A demonstration of dashboard usage, including how to interpret it and use filters to identify root causes.

- Proposed actions based on dashboard insights.

- A conclusion with next steps (e.g., dashboard implementation).

- Added content to story points using existing and new worksheets, constructing dashboards as presentation-style slides.

- Saved a completed Tableau Story version.

- Prepared a 3 to 5-minute presentation of the Tableau Story (screen recording or PDF format).

Deliverables: Worksheets, mock-ups, dashboard template, finalized dashboard, Tableau Story, and a presentation.

### Part 5: Project Submission
The final project submission adhered to specific guidelines for sharing and documentation.

Submission Format: A ZIP archive containing all project files.

- README.md: Included this README.md file with a link to the published Tableau workbook on Tableau Public.

- File Size: Ensured all included files (including additional files) did not exceed 9 megabytes in total.

Key Findings & Recommendations (To be populated based on Tableau Workbook)
(This section would typically be filled with specific insights and recommendations derived from the Tableau visualizations after the analysis is complete. For example:)

- Profit Centers: Identified "Office Supplies - Binders" in the "Central" region as a top profit center, suggesting opportunities for increased focus.

- Loss Makers: Highlighted "Technology - Tables" in the "South" region as a significant loss-maker, indicating a need for re-evaluation or discontinuation.

- Advertising Opportunities: Recommended advertising in "California" during "November" due to high average profit per unit sold, with a suggested ad spend of X% of profits.

- High Return Products: Identified "XYZ Product" as having an abnormally high return rate, suggesting quality control issues or misleading product descriptions.

- Customer Retention: Noted that customers in the "East" region generally have lower return rates, indicating stronger customer satisfaction in that area.

- Return Causes (Sprint 5): Identified [Specific Root Cause 1, e.g., "seasonal spike in returns during holiday months due to gift purchases"] and [Specific Root Cause 2, e.g., "high return rates for certain electronic accessories due to compatibility issues"].

- Recommendations to Reduce Returns (Sprint 5): Proposed [Specific Recommendation 1, e.g., "implementing a clearer return policy for holiday purchases"] and [Specific Recommendation 2, e.g., "enhancing product descriptions and compatibility guides for electronic accessories"].

Tools Used
- Tableau Desktop: For data visualization, dashboard creation, and calculated fields.

- Microsoft Excel (or similar spreadsheet software): For initial data preparation and understanding.
