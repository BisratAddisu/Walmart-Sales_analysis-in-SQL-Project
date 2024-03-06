Walmart Sales Analysis Project
1. Project Overview
* Project Title: Walmart Sales Data Analysis
* Goal of the project: This sample project aims to explore Walmart Sales data to understand top-performing branches and products, sales trends of different products, and customer behavior. The aim is to study how sales strategies can be improved and optimized.
* Dataset(s) used: The dataset was obtained from the Kaggle Walmart Sales Forecasting Competition.
* Tools Used: MySQL,
2. Data Overview
* Source(s) of the Data: The dataset was obtained from the Kaggle Walmart Sales Forecasting Competition.
* Data Size: 132kb
* Brief Description of the Data: This dataset contains sales transactions from three different branches of Walmart, respectively located in Mandalay, Yangon, and Naypyitaw. The data contains 17 columns and 1000 rows:
Column
	Description
	Data Type
	invoice_id
	Invoice of the sales made
	VARCHAR(30)
	branch
	Branch at which sales were made
	VARCHAR(5)
	city
	The location of the branch
	VARCHAR(30)
	customer_type
	The type of the customer
	VARCHAR(30)
	gender
	Gender of the customer making purchase
	VARCHAR(10)
	product_line
	Product line of the product sold
	VARCHAR(100)
	unit_price
	The price of each product
	DECIMAL(10, 2)
	quantity
	The amount of the product sold
	INT
	VAT
	The amount of tax on the purchase
	FLOAT(6, 4)
	total
	The total cost of the purchase
	DECIMAL(10, 2)
	date
	The date on which the purchase was made
	DATE
	time
	The time at which the purchase was made
	TIMESTAMP
	payment_method
	The payment method
	VARCHAR(15)
	cogs
	Cost Of Goods sold
	DECIMAL(10, 2)
	gross_margin_percentage
	Gross margin percentage
	FLOAT(11, 9)
	gross_income
	Gross Income
	DECIMAL(10, 2)
	rating
	Rating
	FLOAT(2, 1)
	3. Data Cleaning and Preparation
* Missing Value Treatment: This is the first step where inspection of data is done to make sure NULL values and missing values are detected and data replacement methods are used to replace missing or NULL values.
1. Build a database
   1. Create a table and insert the data.
   2. Select columns with null values in them. There are no null values in our database as in creating the tables, we set NOT NULL for each field, hence null values are filtered out.
* Feature Engineering: This will help use generate some new columns from existing ones.
1. Add a new column named time_of_day to give insight of sales in the Morning, Afternoon, and Evening. This will help answer the question on which part of the day most sales are made.
2. Add a new column named day_name that contains the extracted days of the week on which the given transaction took place (Mon, Tue, Wed, Thu, Fri). This will help answer the question of on which day of the week each branch is busiest.
3. Add a new column named month_name that contains the extracted months of the year on which the given transaction took place (Jan, Feb, Mar). Help determine which month of the year has the most sales and profit.
4. Data Analysis List
* Product Analysis: Analyze the data to understand the different product lines, the product lines performing best, and the product lines that need to be improved.
* Sales Analysis: This analysis aims to answer the question of the sales trends of the products. The result of this can help us measure the effectiveness of each sales strategy the business applies and what modifications are needed to gain more sales.
* Customer Analysis: This analysis aims to uncover the different customer segments, purchase trends, and the profitability of each customer segment.
5. Business Questions To Answer
* Generic Question:
   1. How many unique cities does the data have?
   2. In which city is each branch?
* Product:
   1. How many unique product lines does the data have?
   2. What is the most common payment method?
   3. What is the most selling product line?
   4. What is the total revenue by month?
   5. What month had the largest COGS?
   6. What product line had the largest revenue?
   7. What is the city with the largest revenue?
   8. What product line had the largest VAT?
   9. Fetch each product line and add a column to those product lines showing "Good", and "Bad". Good if it is greater than average sales
   10. Which branch sold more products than the average product sold?
   11. What is the most common product line by gender?
   12. What is the average rating of each product line?
* Sales:
   1. Number of sales made at each time of the day per weekday
   2. Which of the customer types brings the most revenue?
   3. Which city has the largest tax percentage/ VAT (Value Added Tax)?
   4. Which customer type pays the most in VAT?
* Customer:
   1. How many unique customer types does the data have?
   2. How many unique payment methods does the data have?
   3. What is the most common customer type?
   4. Which customer type buys the most?
   5. What is the gender of most of the customers?
   6. What is the gender distribution per branch?
   7. Which time of the day do customers give the most ratings?
   8. Which time of the day do customers give the most ratings per branch?
   9. Which day of the week has the best average ratings?
   10. Which day of the week has the best average ratings per branch?
6. Final Report and Presentation
* Key Findings:
   * Product Analysis Findings
      * There are six product lines
      * From these product lines, Fashion & Accessories is the most selling product line, followed by Food & Beverages, and Health & Beauty is the least selling product line.
      * By total revenue, Food & Beverages has the largest revenue, followed by Fashion & Accessories, and Health & Beauty has the lowest revenue.
      * The most common payment method used by customers is cash, closely followed by E-wallet and credit cards.
      * January is the month with both the highest total revenue and the highest cost of goods sold. And February is the month with the lowest total revenue and the lowest cost of goods sold. It appears that there is a high correlation between total revenue and cost of goods sold.
      * Naypyitaw is the city with the highest revenue and Mandalay is the city with lowest revenue.
      * On average, branch A sold slightly more than branches B and C.
      * For female customers, Fashion & Accessories is the most common product line whereas Health & Beauty is the most common product line for male customers.
   * Sales Analysis Findings
      * In general, evenings are the time of day where most sales occur, followed by afternoons, and mornings being the last.
      * Members bring slightly higher revenue than normal customers, and also pay slightly more VAT than normal customers.
      * Naypyitaw is the city with the highest VAT rate, and Yangon is the city with lowest VAT rate.
   * Customer Analysis Findings
      * Members are slightly higher in number and also buy slightly more than normal customers.
      * There is an equal gender distribution of customers overall.
      * Afternoons are the time of day where customers give the most ratings.
      * Mondays have the highest average ratings from the days of the week, and Wednesdays have the lowest.
* Limitations of the Analysis:
   * The analysis made in this project is done based on the given sales data of the first three months of the year and for stores found within the three cities mentioned. All the findings of the project are only applicable for the mentioned time frame and the stores found within the three cities.
* Recommendations and Next Steps:
   * The analysis made in this project shows insights from the first three months of the year. However, in order to have a better understanding of the performances, trends, and patterns of sales year round, it is recommended to repeat this analysis for the rest of the months of the year also.