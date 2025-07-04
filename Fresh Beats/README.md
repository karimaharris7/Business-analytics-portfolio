# Business Analytics Project: Superstore Profitability Analysis with Tableau
## Project Overview
This project focuses on a comprehensive business analytics initiative aimed at improving the profitability of a struggling superstore. As a consultant, my role involved leveraging Tableau for data visualization to identify key areas of profit and loss, assess advertising effectiveness, and analyze product return rates. The insights derived are crucial for strategic decision-making to prevent the superstore from facing bankruptcy.

## Problem Statement
The superstore is experiencing financial difficulties, and the objective of this project is to provide data-driven recommendations to increase its profitability. This involves answering critical business questions through detailed data visualization and analysis.

## Data Sources
The primary dataset used for this analysis is Superstore.xls, which contains detailed operational data for the superstore. The analysis also incorporates a Returns table, which needs to be joined with the Orders table for return rate analysis.

## Methodology
The project was structured into four main parts, each addressing a specific aspect of the superstore's operations. For each question, an individual visualization was prepared to justify the conclusions.

### Part 1: Profits & Losses
This section aimed to identify the most significant profit centers and loss-makers within the superstore's operations.

Objective: Pinpoint areas contributing most to profit and loss.

Analysis:

- Identified the two biggest profit centers and two biggest loss-makers among various dimension pairs (e.g., subcategory + region, shipping mode + product ID).

- Determined which specific products the superstore should discontinue selling.

- Selected three product subcategories to focus on and three to stop selling.

Deliverables: Individual visualizations justifying each conclusion.

### Part 2: Advertising Strategy
This part explored the potential return on investment for advertising efforts, considering temporal and geographical factors.

Objective: Identify optimal advertising opportunities and determine a justifiable advertising spend.

Analysis:

- Identified the 3 best combinations of states and months of the year for advertising.

- Created a visualization showing the average profit for each month of the year for these three states.

- Argued for the willingness to pay in advertising for these specific state-month combinations, based on a return on ad spend ratio (willing to spend 1/5 of profits on advertising).

Deliverables: Visualizations and a justification for advertising spend.

### Part 3: Returned Items Analysis
- This section focused on analyzing product return rates to identify problematic products and customer behaviors.

Objective: Understand return patterns and their impact on profitability.

Data Preparation Hint: Ensured the Returns table was LEFT JOINed onto the Orders table, resulting in "Yes" and "null" values in the Returned column.

Calculated Field: Transformed the Returned field into a calculated field where null values were 0 and Yes values were 1.

Analysis:

- Identified products with the highest return rates using a visualization.

- Identified customers with the highest return rates using a visualization.

- Created a separate visualization showing the average profit against the average return rate on a chosen dimension (e.g., state, shipping mode, product type).

- Presented a visual argument for whether the superstore should continue or discontinue business based on this dimension.

Deliverables: Multiple visualizations addressing return rates and their impact.

### Part 4: Project Submission
The final project submission adhered to specific guidelines for sharing and documentation.

- Submission Format: A ZIP archive containing all project files.

- README.md: Included this README.md file with a link to the published Tableau workbook on Tableau Public.

- File Size: Ensured all included files (including additional files) did not exceed 9 megabytes in total.

## Key Findings & Recommendations (To be populated based on Tableau Workbook)
(This section would typically be filled with specific insights and recommendations derived from the Tableau visualizations after the analysis is complete. For example:)

- Profit Centers: Identified "Office Supplies - Binders" in the "Central" region as a top profit center, suggesting opportunities for increased focus.

- Loss Makers: Highlighted "Technology - Tables" in the "South" region as a significant loss-maker, indicating a need for re-evaluation or discontinuation.

- Advertising Opportunities: Recommended advertising in "California" during "November" due to high average profit per unit sold, with a suggested ad spend of X% of profits.

- High Return Products: Identified "XYZ Product" as having an abnormally high return rate, suggesting quality control issues or misleading product descriptions.

### Customer Retention: Noted that customers in the "East" region generally have lower return rates, indicating stronger customer satisfaction in that area.

### Tools Used
- Tableau Desktop: For data visualization, dashboard creation, and calculated fields.

- Microsoft Excel (or similar spreadsheet software): For initial data preparation and understanding.
