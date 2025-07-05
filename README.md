## PROJECT 1
# DSA-Excel-Project
#### File Link: https://docs.google.com/spreadsheets/d/1DEV3-RnVNG8_VuR0mik3damnM4STeV2U/edit?usp=drive_link&ouid=105886618424154552337&rtpof=true&sd=true

#### Excel Sheets Highlight:
1. Sheet 1: Answers to the questions using Pivot Table
2. Sheet 2: Pivot Table for Amazon Product Review dashboard
3. Sheet 3: Dashboard View
4. Sheet 4: Amazon Dataset Table
   
#### Summarization of the Amazon Product Review Dataset
### Purpose

This dataset provides insights into Amazon products, their pricing, discounts, ratings, and customer engagement. The analysis aims to derive actionable insights from Amazon product listings to inform decisions related to pricing, product quality, customer satisfaction, and marketing strategy. This is part of Retail Tech Insights’ mission to help e-commerce sellers grow through data-driven strategies.

### Dataset Overview

* Total Products: 1,465
* Total Columns of original data: 16, including product details, pricing, ratings, and review metadata.

### Key Data Fields

| Column Name                                   | Description                                           |
| --------------------------------------------- | ----------------------------------------------------- |
| `product_id`                                  | Unique identifier for each product                    |
| `product_name`                                | Full product name/title                               |
| `category`                                    | Product categories (may include multiple levels)      |
| `actual_price`                                | Original listed price                                 |
| `discounted_price`                            | Current selling price                                 |
| `discount_percentage`                         | Proportion of discount (`(actual - discount)/actual`) |
| `rating`                                      | Average customer rating (e.g., 4.2)                   |
| `rating_count`                                | Total number of customer reviews                      |
| `about_product`                               | Brief product description                             |
| `user_id`, `user_name`                        | Reviewer info (aggregated)                            |
| `review_id`, `review_title`, `review_content` | User feedback (aggregated)                            | 
| `img_link`, `product_link`                    | Media and purchase URLs                               | Not Used/Can be removed
| `Products with 50%/> Discount`                | Generated using: =IF([@[discounted_price]]>=0.5, 1, 0)|
| `Total Potential Revenue`                     | Generated using: =[@[actual_price]]*[@[rating_count]] |
| `Price Range Bucket`                          |  =IF([@[discounted_price]]<200, "<200", IF([@[discounted_price]]<=500, "200–500", ">500"))  |
| `Rating Count <1000`                          | Generated using: =IF([@[rating_count]]<1000, 1, 0)    |


### How the Analysis Was Done

1. Tool Used: Microsoft Excel

3. Data Preparation Steps:

   * Cleaned and verified column data types (e.g., numeric fields like `rating`, `discount_percentage`)
   * Added calculated columns such as:

     * `Revenue Potential = actual_price × rating_count`
     * `Combined Score = rating × rating_count`
     * `Price Buckets` for grouping products by price
   * Created pivot tables for category-wise aggregation

4. Visualization:

   * Used Pivot Charts (Bar, Column, Pie) to illustrate:

     * Average discounts by category
     * Distribution of ratings
     * Review count and revenue per category
     * Relationship between discount level and rating
     * Top-performing products

5. KPIs Highlighted on Dashboard:

   * Total Products
   * Total Potential Revenue
   * Average Discount Price
##### Slicers
   * Rating
   * Price Range Bucket
   * % of Products with ≥50% Discount

### Key Insights from Analysis

* High-Discount Products tend to receive high customer engagement but not necessarily higher ratings.
* Some categories offer large discounts (up to 90%), which can be leveraged in promotions.
* A significant number of products have fewer than 1,000 reviews, indicating limited visibility or popularity.
* Top-rated products are not always the most-reviewed, suggesting potential for review campaigns to boost credibility.
* Average discounts vary by category, indicating pricing flexibility in some product segments.

### Suggestions for Product Development & Improvement

1. Optimize Discount Strategy

   * Consider targeted discount campaigns in categories where average ratings remain high despite deep discounts.

2. Boost Under-Reviewed Products

   * Launch engagement campaigns (e.g., discounts for reviews) to increase visibility and credibility of products with low review counts.

3. Improve Product Listings

   * Enhance titles, images, and descriptions based on content analysis of high-performing products.

4. Focus on High-Revenue Categories

   * Allocate resources to categories generating higher potential revenue to maximize return on investment.

5. Track Rating-Discount Balance

   * Avoid excessive discounts on poorly-rated products without quality improvements, as this can damage brand perception.

### Conclusion

The Excel-based analysis of Amazon product data provided valuable insights into pricing trends, customer engagement, and category performance. These findings can help guide product development decisions, enhance marketing effectiveness, and boost customer satisfaction on Amazon.
```
```
## PROJECT 2 - POWER BI

# DSA-Power-BI-Project

### Palmoria Group HR Data Analysis — Summarization

#### Project Background

Palmoria Group, a Nigerian manufacturing company, has come under public scrutiny due to allegations of gender inequality across its three regions. With the goal of expanding internationally, the leadership is eager to address any structural issues — especially those related to gender distribution, salary disparity, and compliance with new wage regulations. As an HR analytics consultant, I was engaged to conduct a comprehensive analysis of the company’s HR data and provide actionable insights.

### Data Cleaning and Preparation

Using Power BI Power Query, the following data quality issues were resolved:

* Removed employees with missing salaries (exited staff).
* Filtered out departments labeled “NULL.”
* Standardized the gender field by labeling all blanks as “Undisclosed.”

Additionally, bonus rules were cleaned by unpivoting department-based percentage ratings for easier mapping during bonus allocation.

### Key Insights Delivered

#### Gender Distribution Analysis

* Gender representation was visualized across departments and regions.
* A stacked column chart and donut chart revealed gender imbalances, particularly underrepresentation of women in certain departments and regions.

#### Performance Rating by Gender

* Ratings such as “Very Good,” “Good,” etc., were analyzed by gender.
* A 100% stacked bar chart exposed inconsistencies in how male and female employees are rated, potentially signaling bias.

#### Gender Pay Gap

* The average salary for each gender was computed and visualized.
* A **matrix visual** by department and region showed significant pay disparities favoring male employees in specific locations and units.

#### Salary Compliance and Distribution

* Employees were grouped into salary bands of \$10,000 increments.
* A salary band distribution chart revealed the majority of employees earn below the regulatory threshold of \$90,000.
* A KPI card calculated the number of non-compliant salaries.

#### Bonus Calculation and Total Pay

* Using the department and performance rating, bonus percentages were assigned to each employee.
* Bonus amounts were calculated and added to the base salary to determine Total Pay.
* A region-wise breakdown of total payouts and bonus sums was presented to guide budgeting.

### Technical Tools and Features Used

* Power Query: for cleaning, filtering, and unpivoting data
* DAX Measures: for salary bands, bonus computations, and compliance metrics
* Visuals: Donut charts, stacked columns, KPI cards, matrices, and salary distribution histograms
* Filtering: Slicers by region, department, and gender enabled interactive exploration

### Recommendations for Management

* Investigate departments and regions where gender imbalance and pay gaps are most pronounced.
* Establish internal policies to ensure rating fairness across all genders.
* Enforce the \$90,000 minimum salary regulation to meet compliance and ethical standards.
* Review bonus allocation models for fairness and consistency.

### Conclusion

This analysis equips Palmoria’s management with critical insights to foster gender equity, ensure regulatory compliance, and create a data-driven roadmap for HR transformation. These insights are essential for enhancing employee satisfaction, brand perception, and long-term global expansion.

Attached is the pdf file link; https://drive.google.com/file/d/17Ntne1CurVZEVzsPcyUmO1fiwEhxzVs4/view?usp=drive_link and the 
power BI file link; https://drive.google.com/file/d/1cmOsg6njUa2RmVYQ2JSQwVcL2p7AdvGy/view?usp=drive_link
https://www.linkedin.com/in/abimbola-ige-6a7377287
```


