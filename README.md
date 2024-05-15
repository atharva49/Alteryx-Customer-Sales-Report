# Alteryx-Customer-Sales-Report

This repository contains an Alteryx workflow designed to generate a Customer Sales Report. The workflow processes data from customer and transaction files, identifies specific customer segments, and produces various output reports. The following sections provide detailed information about the workflow components, data sources, and outputs.

Workflow Overview
The Alteryx workflow is designed to:

Filter customers who have responded "No" to a specific query.
Join transaction data with customer data.
Generate reports for:
Total sales in descending order.
Transactions not joined to customers.
Customers who responded "No" but made a transaction.
Data Sources
Input Files
Customers.csv: Contains customer data.
Transactions.xml: Contains transaction data.
Output Files
CustomerSalesReportBySegment.xlsx: Excel report with the top 10 customers by total sales.
Customers_who_responded_no_but_made_transaction.csv: CSV file listing customers who responded "No" but made a transaction.
Workflow Details
Steps
Read Customers Data:

Input: Customers.csv
Operation: Read the customer data.
Filter Customers:

Condition: [Responder] = "No"
Operation: Filter customers who responded "No".
Read Transactions Data:

Input: Transactions.xml
Operation: Read the transaction data.
Summarize Transactions:

Operation: Calculate total sales for each customer.
Join Data:

Operation:
Join customers with transactions on customer ID.
Identify transactions not joined to customers.
Identify customers who responded "No" but made a transaction.
Sort and Select:

Operation:
Sort total sales in descending order.
Select the top 10 customers by total sales.
Output Reports:

Output:
Write the sorted sales report to CustomerSalesReportBySegment.xlsx.
Write the list of specific customers to Customers_who_responded_no_but_made_transaction.csv.
Workflow Components
Input Data Tool: Reads data from CSV and XML files.
Filter Tool: Filters data based on specific conditions.
Summarize Tool: Aggregates data to calculate total sales.
Join Tool: Joins datasets based on common fields.
Sort Tool: Sorts data in descending order.
Select Tool: Selects the top N rows.
Output Data Tool: Writes data to CSV and Excel files.
How to Run the Workflow
Ensure you have Alteryx installed on your machine.
Open the Alteryx Designer.
Load the workflow file (.yxmd).
Make sure the input files (Customers.csv and Transactions.xml) are placed in the specified directories.
Run the workflow.
Check the output files for the generated reports.

![Alteryx_finance_workflow](https://github.com/atharva49/Alteryx-Customer-Sales-Report/assets/56105570/2e42fb9f-77a1-4cd3-a55e-a31871e385d2)
