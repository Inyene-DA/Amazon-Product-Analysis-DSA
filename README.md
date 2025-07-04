# Amazon-Product-Analysis-DSA
Exploring the full Potential of Excel as a tool for Data Analysis with this project on Amazon Product Data. 

# Project Overview
- This project analyzes the Amazon Products at RetailTech Insights to provide business insights through exploratory data analysis and interactive Dashboard. The Project contained 1465 rows and 16 columns. 
- The Project focused on product distributions, customer reviews, and profitability with regards to Sales revenues. 
- Datasets used for the project included records such as;
  - Product details: name, category, price, discount, and ratings
  - Customer engagement: user reviews, titles, and content
  - Each row represents a unique product, with aggregated reviewer data stored as comma-separated values


# Main Highlights Explored
1. Product Profitability: Identifying which Products and Product Category drive the highest sales with consequent increase in demand.
3. Customer Satisfaction: Measuring customers satisfaction with the number of reviews and review counts by Products and Product Category.
4. Reviews and Ratings: Measuring how these indices greatly impacts the sales revenue. A satisfied customer will always advertize a good product or happily increase product sale.

# Tools Used
- Excel: For cleaning Dataset, Annalysis
- Pivot Table: For creating Tables and making Data Charts
- Dashboard: For Visualizing

# Data Processing
# The Workflow included:
  1. Data Importation
  2. Data cleaning and Standardized formatting
    - Duplicates were removed, converted text to column, and missing values handled where applicable. This was done to ensure records contained, maintained data integrity and prevent errors during analysis.
       - TRIM(B2): Product Name Shortening to reduce long product name and product category for cleaner charts
       - =PROPER(C2): Removing extra spaces to achieve clean text fields
       - Delimiter: Using text-to-columns with delimiter such as; "|" , "space", to simplify product Category and Product names.
       - Helper Columns: All calculated columns and cleaning columns used to achieve final analysis, pivot table and dashboard.  

# Data Analysis Questions
  - Below are questions answered from the dataset to give insight to the business need and recommendations.
    
  ##  1:  What is the average discount percentage by product category?
![Amazon Product Analysis 1_DSA](https://github.com/user-attachments/assets/2187eac5-5ef7-481e-ad7d-7ad8ce459c59)

  - Used a Pivot Table:
  - Rows: Product Category
  - Values: Average of Discount %


  ## 2: How many products are listed under each category?
![image](https://github.com/user-attachments/assets/9b508d0a-98d5-4c2e-98e4-c10a432ea255)

  - Used a Pivot Table:
  - Rows: Product Category
  - Values: Count of Product Name


  ## 3: What is the total number of reviews per category?
![image](https://github.com/user-attachments/assets/c4991e8f-988c-478d-a5d4-f4abef6ad009)

  - Used a Pivot Table:
  - Rows: Product Category
  - Values: Sum of Rating Count


  ## 4: Which products have the highest average ratings?
![image](https://github.com/user-attachments/assets/38b49ff8-67cd-47ea-ae06-442ae6fac434)

  - Used a Pivot Table:
  - Rows: Product Name
  - Values: Average of Rating
  - Sort: Descending by Average Rating
  - Filter: Leaving Top 3 with same Average rating


  ## 5: What is the average actual price vs the discounted price by category?
![image](https://github.com/user-attachments/assets/0feea446-a6b2-4588-8449-9c7358333962)

  - Used a Pivot Table:
  - Rows: Product Category
  - Values: Average of Actual Price, Average of Discounted price
  - Sort: Descending by Average Rating


  ## 6: Which products have the highest number of reviews?
![image](https://github.com/user-attachments/assets/4a27924d-c3e9-47b0-b525-b925d8db97c9)

  - Used a Pivot Table:
  - Rows: Product Name
  - Values: Sum of Rating Count
  - Sort: Descending by Rating Count
  - KPI Custom formatting: #,##0,,,"m"


  ## 7: How many products have a discount of 50% or more?

  -  Used a calculated column to get 662
  - Function: =IF(Discount%>=50%, "1","0")
  - Used a Pivot Table
  - Rows: Product Name
  - Values: Sum of Helper Column


  ## 8: What is the distribution of product ratings (e.g., how many products are rated 3.0, 4.0, etc.)?

![image](https://github.com/user-attachments/assets/21b82416-176c-452e-92d8-144dee9ae93c)

  - Used a Pivot Table
  - Rows: Rating
  - Values:Count of Product ID


  ## 9: What is the total potential revenue (actual_price × rating_count) by category?
![image](https://github.com/user-attachments/assets/e3aeec92-dcff-4c77-a662-46f9325b26b1)

  - Calculated Column Function to get Total Potential Revenue:
    =[@[Actual Price]]*[@[Rating Count]
  - Pivot Table:
  - Rows: Product Category
  - Values: Sum of Total Revenue
  - KPI Custom formatting: #,##0,,,"b"


  ## 10: What is the number of unique products per price range bucket? 
![image](https://github.com/user-attachments/assets/3215076a-2f78-47b4-9030-cddbba84a65f)

  - Calculated Column: =IF(D2<200,"<$200",IF(D2<=500,"$200-$500",IF(D2<10000,"<$10000",">$10000")))
  - Pivot Table:
  - Rows: Price Range Bucket
  - Values: Count of Product Name


  ## 11: How does the rating relate to the level of discount?
![image](https://github.com/user-attachments/assets/3967f100-aac8-443e-923f-77cc465dd537)

  - Pivot Table:
  - Rows: Discount %
  - Values: Average Rating
  - The chart highlights the trend of average rating across discounts ranges.


## 12: How many products have fewer than 1,000 reviews?
![image](https://github.com/user-attachments/assets/3779e237-4527-4d24-9b10-01cd027f0815)

  - Pivot Table: 
  - Rows: Rating Count (Group function 0-999)
  - Values: Count of product ID


  ## 13: Which categories have products with the highest discounts?
![image](https://github.com/user-attachments/assets/fde5765d-7e59-4edc-9175-f1cf1d989b13)
  
  - Pivot Table: 
  - Rows: Product Category
  - Values: Max of Discount%


  ## 14: Identify the top 5 products in terms of rating and number of reviews combined.
![image](https://github.com/user-attachments/assets/2f00b492-7697-4134-97c7-a7b774fd5592)

  - Created a calculated column
    - Formula: =([@[Rating]]*[@[Rating Count]])
  - Pivot Table: 
  - Rows: Product Name
  - Values: Sum of Score
  - Filter: Top 5
  - Sort: Descending


# Dashboard Features
  ## Section Details:
    - KPI Cards: Total Products Counts, Total Potential Revenue, Rating Count, Interactive Slicers to gain insights on the Product Category, Clustered Columns, Pie Charts, Line charts.

# Skills Included
  - Data Cleaning, Data Analysis, Data Visualization, Statistics.

# Results:
  - This data analysis shows the evident growing demand for Electronics with The Amazon High Speed Product within the Electronics Category generating the highest reviews and rating. Hence products like that should always be in sufficient stock.
  - Customers feedback concerning the other products in less demand should be highly encouraged and addressed accordingly.
  - More stretegic campaigns of products upon new release should be in place to create awareness of products with less ratings or reviews.
    
  - The Dashboard below contains the charts derived from the pivot tables.

![Amazon Product Analysis_DSA](https://github.com/user-attachments/assets/548c5b0a-f5df-45ac-bedd-7df2dcf86d7d)







