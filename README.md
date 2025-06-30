# DSA-Excel-Project
Summarization of the Amazon Product Review Dataset
### 🔍 **Purpose**

This dataset provides insights into Amazon products, their pricing, discounts, ratings, and customer engagement. It's designed to help businesses improve their product strategy, marketing efforts, and customer experience on e-commerce platforms.

### 📊 **Dataset Overview**

* **Total Products:** 1,465
* **Total Columns:** 16
* **Source:** Amazon product listings (scraped data)

### 🗂️ Key Data Fields

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

### 💡 Insights I Derived

1. Pricing Strategy: Understand average discounts and pricing by category.
2. Customer Engagement: Analyze review volume and content to spot trends.
3. Product Performance: Identify top-rated, most-reviewed, or best-selling products.
4. Revenue Potential: Estimate earnings using ratings and price data.
5. Category Performance: Compare product count, ratings, and revenue by category.


### 📁 Cases

* Marketing & Promotion Planning
* Product Listing Optimization
* Competitor Analysis
* Customer Satisfaction Monitoring
* Inventory & Revenue Forecasting

