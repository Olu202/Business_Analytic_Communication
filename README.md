**Payment Analysis Dashboard**

**Introduction**

This guide provides step-by-step instructions to analyze and visualize payment data. You will learn how to prepare your dataset, perform data analysis, and create visualizations to provide insights into payment behaviors. The final output will be a dashboard with multiple plots to help stakeholders understand trends, frequent delinquents, and customer behaviors related to late payments.

**Prerequisites**

Before you start, ensure you have the following installed:

Python 3.x
pandas
seaborn
matplotlib
You can install the required libraries using pip:

**Steps to Achieve the Analysis and Visualizations**

**1. Prepare Your Dataset**

Ensure your dataset is in CSV format and contains the following columns:

Customer_ID
Document Number
Document Date
Net due date
Amount in doc. curr.
Document type
Local Currency
Posting Date
Payment date
Invoice reference
Document currency
Eff.exchange rate
Clearing Document
Name 1
Days to Pay
Invoice Amount
Late Payment
Is_Late_Payer

**2. Load and Prepare the Data**

Load the dataset into a pandas DataFrame.
Convert the Posting Date, Net due date, and Payment date columns to datetime format.
Create a Late Payment column indicating whether the payment was late.
Create a Days Late column to calculate the number of days a payment was late.

**3. Create a Line Graph of Late Payments Trend**

Aggregate the number of late payments by month.
Plot the trend using matplotlib.

**4. Generate Summary Statistics for Top Customers**
   
Group the data by customer (Name 1) and calculate summary statistics: total invoice amount, total number of invoices, average payment days, number of late payments, and number of on-time payments.
Select the top 10 customers based on total invoice amount.
Visualize the summary statistics using a heatmap with seaborn.

**5. Create a Bar Chart of Average Payment Delay by Quarter**
   
Extract the year and quarter from the Payment date.
Filter the data for the past year.
Calculate the average payment delay by quarter.
Plot the average payment delay using a bar chart with matplotlib.

**6. Identify and Visualize Frequent Delinquents**

Calculate the number of late payments for each customer.
Set a threshold to identify frequent delinquents.
Plot the number of late payments for frequent delinquents using a bar plot with seaborn.

**7. Create a Dashboard**

Combine all the above visualizations into a single dashboard using matplotlib's subplot functionality.
Arrange the plots in a 2x2 grid for comprehensive visualization.

**8. Display the Dashboard and Results**

Run the final script to generate the dashboard.
Print the details of the customer with the highest number of late payments.
Print the list of frequent delinquents based on the set threshold.
