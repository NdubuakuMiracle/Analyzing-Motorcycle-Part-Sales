# Motorcycle Parts Sales Data Analysis  

## Overview  

You're working for a company that sells motorcycle parts, and they've asked for some help in analyzing their sales data!

They operate three warehouses in the area, selling both retail and wholesale. They offer a variety of parts and accept credit cards, cash, and bank transfer as payment methods. However, each payment type incurs a different fee.

The board of directors wants to gain a better understanding of wholesale revenue by product line, and how this varies month-to-month and across warehouses. You have been tasked with calculating net revenue for each product line and grouping results by month and warehouse. The results should be filtered so that only "Wholesale" orders are included.

## Dataset Description  

The analysis was based on the sales data contained in a table named `sales`, which includes the following columns:  

- **order_number** (VARCHAR): A unique order number.  
- **date** (DATE): The date of the order, which ranges from June to August 2021.  
- **warehouse** (VARCHAR): The warehouse from which the order was processed—North, Central, or West.  
- **client_type** (VARCHAR): Indicator of whether the order was Retail or Wholesale.  
- **product_line** (VARCHAR): The type of product ordered.  
- **quantity** (INT): The number of products ordered.  
- **unit_price** (FLOAT): The price per product in dollars.  
- **total** (FLOAT): The total price of the order in dollars.  
- **payment** (VARCHAR): The payment method used—Credit card, Transfer, or Cash.  
- **payment_fee** (FLOAT): Percentage fee deducted from the total based on the payment type.  

## Methodology  

To derive meaningful insights, I executed the following steps:  

1. **Data Extraction**: I accessed the sales database to retrieve the relevant data from the `sales` table.  
  
2. **Filtering**: I filtered the dataset to include only 'Wholesale' orders, ensuring that my analysis focused solely on wholesale revenue.  
  
3. **Net Revenue Calculation**: For each order, I calculated the net revenue by applying the payment fee to the total price. The formula I used was:  
   \[  
   \text{net\_revenue} = \text{total} - (\text{total} \times \text{payment\_fee})  
   \]  

4. **Date Formatting**: I extracted the month from the order date to facilitate monthly grouping in the analysis.  

5. **Grouping and Aggregation**: I aggregated the net revenue by `product_line`, `month`, and `warehouse`, allowing me to analyze wholesale revenue trends across different dimensions.  

6. **Query Output**: Finally, I structured the output in the required format, displaying the results clearly to reflect the net revenue per product line on a month-to-month basis across warehouses.  

## Conclusion  

By performing a thorough analysis of the motorcycle parts sales data, I produced insights that can help the board of directors understand the dynamics of their wholesale revenue more effectively. The results I generated provide a clearer view of how revenue varies by product line, month, and warehouse, potentially informing strategic decisions moving forward.
