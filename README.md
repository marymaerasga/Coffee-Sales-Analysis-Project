# Coffee Sales Analysis Project
Sales 2019-2022

This is my second project as I continue applying what I've learned from my self-study in Microsoft Excel and data analytics.

## Project Overview
This Coffee Sales Analysis Project aims to explore, analyze, understand trends and patterns in coffee sales across different coffee types, roast levels, sizes, country, and year (2019-2022). By analyzing sales data, the project identifies sales over time,  which types of coffee are most popular, observes seasonal trends, and explores variations in customer preferences. The findings from this project can be used to inform business strategies, guide marketing efforts, and support product development. The analysis provides insights into the coffee market and offers recommendations for optimizing sales and targeting key customer segments.

## Data
This is a dataset from Kaggle, which have 3 table such as:

Order - Order ID, Order Date, Customer ID, Product ID, Quantity

Customer - Customer ID, Customer Name, Email, Phone Number, Address Line 1, City, Country, Postcode, Loyalty Card

Product - Product ID, Coffee Type,	Roast Type,	Size,	Unit Price,	Price per 100g,	Profit

![image](https://github.com/marymaerasga/Coffee-Sales-Analysis-Project/assets/86357387/4129bc95-625c-4706-8fcd-e9f28a0621af)

![image](https://github.com/marymaerasga/Coffee-Sales-Analysis-Project/assets/86357387/c2389bb6-196e-4101-8217-baf0383564e2)

![image](https://github.com/marymaerasga/Coffee-Sales-Analysis-Project/assets/86357387/ae839de3-af1d-447d-b1c4-cd4bcb57a467)


## Exploratory Analysis Process

### Data Preparation:

As a Data Analyst, I must thoroughly examine the data to ensure it is well-formatted, clean, and ready for analysis.

- Merge Tables
Since there are three tables, the first thing I did was merge them. Data needed for analysis were in different tables—Customers and Products—so I used the INDEX/MATCH function to add them to the Orders table. The extracted data included Customer Name, Email, Country, and Loyalty Card from the Customers table, as well as Coffee Type, Roast Type, Size, and Unit Price from the Products table.

- Clean Data:
After merging the tables , I clean the data to be ready for analysis. Such as
1. Data Formatting: Since the Coffee Type and Roast Type data were in abbreviations, I renamed them using the IF function to make the data easier to read. For example, IF(A2 = 'Lib', 'Liberica', IF(A2 = 'Ara', 'Arabica', IF(A2 = 'Rob', 'Robusta', IF(A2 = 'Exc', 'Excelsa', ' ')))). I also formatted the Size field by customizing the number format to include 'kg', making it more readable.
2. I Extracted the years and months from the Order Date using the formula TEXT() and YEAR(), and created a new column for that.
3. Sales calculated using (Unit Price*Quantit)
4. Converted the data to a table
5. Check duplicates: Since there's no duplicates , its good to go for data analysis.
   
### Data Analysis:

Sales Over Time 

![image](https://github.com/marymaerasga/Coffee-Sales-Analysis-Project/assets/86357387/0d9102a7-8283-4070-aac0-4a4bc64180df)

This table shows total sales for all coffee types increased each year from 2019 to 2021. Arabica became the top-selling coffee in 2021, overtaking Excelsa, which had been leading in 2019 and 2020. In 2022, there was a notable drop in total sales across all coffee types. Arabica still led, but its total sales dropped significantly compared to the previous year. I think it because the sales  month in the year 2022 are Jan-Aug , ask  for the Sep-Dec month sales and do the analysis further.


Top 5 Customers

![image](https://github.com/marymaerasga/Coffee-Sales-Analysis-Project/assets/86357387/8a94327f-a4b3-4a16-a804-5c9e43bd1996)

This table shows the top 5 customers thus Allis Wilmore has the highest sales, with a total of $317. The sales figures are relatively close among the other customers. Brenn Dundredge is the second-highest with $307, followed by Terri Farra with $289. The sales difference between the top and bottom customers is not vast. Nealson Cuttler and Don Flintiff have $282 and $278, respectively.

Sales by Country

![image](https://github.com/marymaerasga/Coffee-Sales-Analysis-Project/assets/86357387/0bb79dec-f10e-4cc5-8f65-a9a73d4797b9)

The United States leads by a wide margin, with $35.64k in total sales.Ireland has the second-highest sales at $6.70k, while the United Kingdom follows with $2.80k. The gap between the United States and the other two countries is substantial, indicating a significantly larger market or customer base.


## Dashboard

![image](https://github.com/marymaerasga/Coffee-Sales-Analysis-Project/assets/86357387/3fbc6f69-406e-4218-8b28-091d58d605ce)


