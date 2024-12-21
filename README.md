# Pizza-Sales-Report-Dashboard
# Dashboard Link - https://app.powerbi.com/links/z3jf4yZbjK?ctid=a1a4ee51-99fa-437d-8ba7-d05192f6c077&pbi_source=linkShare&bookmarkGuid=16519565-9261-49be-b22b-9654582e7865

This report analyzes pizza sales data to help the company improve operations, enhance customer satisfaction, and optimize sales performance. The report was created in Power BI Desktop and subsequently published to Power BI Service. Key insights, metrics, and visualizations were derived to assist the company in identifying areas for improvement and making data-driven decisions.



Step 1: Load Data into Power BI and Clean in Power Query
The first step in creating the Pizza Sales Analysis Dashboard was to load the data into Power BI and perform initial cleaning in Power Query to prepare the dataset for analysis.

Loading Data into Power BI:
The dataset, which was provided in a CSV format, was loaded into Power BI Desktop. This is the first crucial step in any Power BI project, as the data needs to be imported into the Power BI environment for further processing and visualization.

Open Power BI Desktop.
From the "Home" tab, click on the "Get Data" button and select "Text/CSV" from the list of data sources.
Browse and select the CSV file containing the pizza sales data.
Click "Load" to bring the data into Power BI.
Cleaning Data in Power Query:
Once the data was loaded into Power BI, it was essential to clean and prepare it for analysis. This was done using Power Query Editor, which provides an intuitive interface for data transformation tasks such as handling missing values, correcting data types, and filtering unnecessary records.

Accessing Power Query Editor:

From the Power BI Desktop interface, select "Transform Data" to open Power Query Editor.
Data Profiling:

In the Power Query Editor, data profiling options were enabled to help identify errors, missing values, and data quality issues.
Under the "View" tab, the following profiling options were enabled:
Column Distribution: Displays the distribution of values in each column to identify any anomalies.
Column Quality: Shows the percentage of valid, empty, and error values for each column.
Column Profile: Provides a more detailed view of the data, including basic statistics like minimum, maximum, average, and unique values.
Handling Null and Missing Values:

In this dataset, there were no significant issues with missing or null values, except in some columns like Delivery Time and Processing Time.
Any null or missing values in the Delivery Time column were either replaced or removed, based on the specific context of the analysis (e.g., rows with missing values for delivery times were excluded from calculations).
Data Type Correction:

Ensured that all columns had the correct data types for analysis. For example, the Order Date column was set to the Date type, and the Total Sales column was set to Currency.
Some columns were identified as containing errors, and these were cleaned up by either removing erroneous rows or correcting the data format.
Additional Data Transformation:

Additional columns, such as Customer Age Group, were calculated using Power Query’s custom column functionality, where an expression was used to classify customers into age brackets.
Filtered out irrelevant or unnecessary columns that wouldn’t contribute to the analysis, such as internal IDs or excessive metadata.
Final Data Review:

After performing the necessary transformations and cleaning, the dataset was reviewed to ensure that it was ready for the next steps of the analysis.
The cleaned dataset was then loaded back into Power BI for further modeling and visualization.
By performing these data preparation steps in Power Query, the dataset was made ready for detailed analysis and visualizations, ensuring that the insights derived would be accurate and reliable.





Metrics and Calculations:
Step 1: Key Sales Metrics and Average Ratings
Key metrics affecting customer satisfaction and sales performance were identified and analyzed. These metrics included average ratings, sales volume, order processing times, and customer feedback.

The following parameters and average ratings were recorded:

Order Fulfillment Time: 4.12/5
Delivery Time: 3.85/5
Pizza Quality: 4.55/5
Online Ordering Experience: 4.02/5
Customer Support: 3.75/5
Payment Process: 4.10/5
Promotions & Discounts: 3.95/5
Packaging Quality: 4.25/5
Menu Variety: 4.00/5
Step 2: Key Visualizations Added to the Dashboard
Brand Name and Tagline:

Displayed using text boxes for easy branding.
Pizza Category Breakdown:

Created pie charts to visualize sales data by pizza category (e.g., Veg, Non-Veg, Margherita, Pepperoni).
Sales Trends by Day and Time:

A line chart was created to track sales trends by day of the week and time of day to understand peak sales hours.
Customer Feedback by Rating:

A bar chart visual was used to represent customer satisfaction levels (Satisfied, Neutral, Unsatisfied) by customer gender and pizza type.
Top-Selling Pizzas:

A table was added to showcase the top 10 best-selling pizzas, with sales quantity and total revenue.
Step 3: Total Sales Calculation
A measure was created to calculate the total sales amount:

DAX
Copy code
Total Sales = SUM(pizza_sales_data[Total Amount])
The total sales amount was represented via a card visual to give a clear summary of the company's revenue.
Step 4: Customer Segmentation by Age and Gender
Using the DAX formula below, customers were segmented by age and gender to understand their preferences:

DAX
Copy code
Age Group = 
IF(pizza_sales_data[Age] <= 25, "0-25 (25 included)", 
IF(pizza_sales_data[Age] <= 50, "25-50 (50 included)", 
IF(pizza_sales_data[Age] <= 75, "50-75 (75 included)", "75-100 (100 included)")))
Step 5: Average Delivery Time and Processing Time
To understand operational efficiency, the average delivery time and processing time were calculated:

DAX
Copy code
Average Delivery Time = AVERAGE(pizza_sales_data[Delivery Time])
Average Processing Time = AVERAGE(pizza_sales_data[Processing Time])
Insights from the Dashboard:
1. Total Sales and Performance:
Total Sales: $1,200,000 (for the given period)
Satisfied Customers (Male): 55%
Satisfied Customers (Female): 45%
Neutral/Unsatisfied Customers (Male): 35%
Neutral/Unsatisfied Customers (Female): 40%
Thus, a higher percentage of customers are satisfied, but there is still a significant proportion of dissatisfied or neutral customers, indicating room for improvement.
2. Average Ratings:
Order Fulfillment Time: 4.12/5
Delivery Time: 3.85/5 (Key area for improvement)
Pizza Quality: 4.55/5 (High satisfaction)
Online Ordering Experience: 4.02/5
Customer Support: 3.75/5 (Needs attention)
Packaging Quality: 4.25/5 (Positive feedback)
3. Sales Trends and Peak Hours:
The highest sales occur on Friday and Saturday evenings.
Peak order times are between 7 PM and 9 PM, indicating when delivery staff and kitchen operations should be optimized.
4. Top-Selling Pizzas:
The top three best-selling pizzas are Pepperoni, Margherita, and BBQ Chicken.
Promotions should focus on these top sellers for increased sales and customer satisfaction.
5. Customer Segmentation and Preferences:
25-50 Age Group: Makes up 60% of customers and prefers Non-Veg pizzas.
Younger Customers (0-25): Prefer Veg pizzas and respond well to discounted offers.
6. Delivery Times and Bottlenecks:
Average Delivery Time: 35 minutes (Need to aim for 30 minutes or less)
Average Processing Time: 8 minutes (Process is efficient but needs to be further optimized during peak times).
Recommendations:
Improve Delivery Efficiency:

Focus on reducing delivery time, especially during peak hours (7-9 PM).
Consider expanding delivery staff during high-demand periods (weekends and evenings).
Enhance Customer Support:

Implement a live chat feature on the website and app to handle customer queries and complaints more efficiently.
Promotions and Discounts:

Target the 25-50 age group with special offers for Non-Veg pizzas.
Launch discounts or combo offers for the 0-25 age group who favor Veg pizzas.
Operational Optimization:

Streamline the online ordering process to make it faster and more user-friendly.
Offer personalized discounts based on previous orders and pizza preferences.
Focus on High-Quality Products:

Maintain the high quality of the Pepperoni and Margherita pizzas, which are the top sellers.
Ensure packaging quality continues to meet customer expectations.
By following these recommendations, the company can optimize sales, enhance customer satisfaction, and improve operational efficiency.

