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
The Workflow included:
  1. Data Importation/ Data cleaning and formatting
    - Duplicates were removed, converted text to column, and missing values handled where applicable. This was done to ensure records          contained, maintained data integrity and prevent errors during analysis.
    - Field formats were Standardized to apropriate data types to avoid errors during analysis.

# Data Analysis
  ## Question #1:
![Amazon Product Analysis 1_DSA](https://github.com/user-attachments/assets/2187eac5-5ef7-481e-ad7d-7ad8ce459c59)


What is the average discount percentage by product category?
Used a Pivot Table
Rows: Product Category
Values: Discount % summarized by average


  ## Question #2:
![image](https://github.com/user-attachments/assets/9b508d0a-98d5-4c2e-98e4-c10a432ea255)

How many products are listed under each category?



  ## Question #3:
![image](https://github.com/user-attachments/assets/c4991e8f-988c-478d-a5d4-f4abef6ad009)

What is the total number of reviews per category?



  ## Question #4:
![image](https://github.com/user-attachments/assets/38b49ff8-67cd-47ea-ae06-442ae6fac434)

Which products have the highest average ratings?



  ## Question #5:
![image](https://github.com/user-attachments/assets/0feea446-a6b2-4588-8449-9c7358333962)

What is the average actual price vs the discounted price by category?



  ## Question #6:
![image](https://github.com/user-attachments/assets/4a27924d-c3e9-47b0-b525-b925d8db97c9)

Which products have the highest number of reviews?



  ## Question #7:
How many products have a discount of 50% or more?
Used a calculated column to get 662
function: IF(Discount%>=50%, "Yes","No")
=COUNTIF(Table2[Products with >=50% Discount],"Yes")


  ## Question #8:
What is the distribution of product ratings (e.g., how many products are rated 3.0, 4.0, etc.)?
![image](https://github.com/user-attachments/assets/21b82416-176c-452e-92d8-144dee9ae93c)


  ## Question #9:
![image](https://github.com/user-attachments/assets/e3aeec92-dcff-4c77-a662-46f9325b26b1)

What is the total potential revenue (actual_price × rating_count) by category?
Created a calculated column to get Total Revenue before using Pivot Chart



  ## Question #10:
![image](https://github.com/user-attachments/assets/3215076a-2f78-47b4-9030-cddbba84a65f)

What is the number of unique products per price range bucket? (e.g., <₹200, ₹200–₹500, >₹500)?
Here i decided to use a price bucket range of $200-$500, <$10000, <$200, >$10000



  ## Question #11:
![image](https://github.com/user-attachments/assets/3967f100-aac8-443e-923f-77cc465dd537)

How does the rating relate to the level of discount?
The chart highlights the trend of average rating across discounts ranges.




## Question #12:
![image](https://github.com/user-attachments/assets/3779e237-4527-4d24-9b10-01cd027f0815)

How many products have fewer than 1,000 reviews?



  ## Question #13:
![image](https://github.com/user-attachments/assets/fde5765d-7e59-4edc-9175-f1cf1d989b13)
  
Which categories have products with the highest discounts?



  ## Question #14:
![image](https://github.com/user-attachments/assets/2f00b492-7697-4134-97c7-a7b774fd5592)

Identify the top 5 products in terms of rating and number of reviews combined.
Creation of calculated column
formula: =([@[Rating]]*[@[Rating Count]])



# Dashboard Features
  ## Section Details:
    - KPI Cards: Total Products Counts, Total Potential Revenue, Rating Count , interactive Slicers to gain insights on the Product Category.

# Skills Included
  - Data Cleaning, Data Analysis, Data Visualization.

# Results:
This data analysis shows the evident growing demand for Electronics with The Amazon High Speed generating the highest reviews and rating. Hence products like that should always be in sufficient stock. Customers feedback concerning the other products in less demand should be highly encouraged and addressed accordingly. 
The Dashboard below contains the charts derived from the pivot tables.

![Amazon Product Analysis_DSA](https://github.com/user-attachments/assets/548c5b0a-f5df-45ac-bedd-7df2dcf86d7d)







