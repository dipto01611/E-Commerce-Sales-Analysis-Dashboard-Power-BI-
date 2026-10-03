# E-Commerce Sales Analysis Dashboard (Power BI)

A four-page Power BI dashboard that analyses one year (2025) of online store orders from all eight divisions of Bangladesh. It shows what sells, what makes a profit, who buys, where they live, and how they pay.


## Tools Used

- **Power BI Desktop**: data model, DAX measures and dashboard
- **Power Query**: data cleaning and transformation
- **DAX**: calculated measures and columns

## Dataset

Two CSV files linked by **Order ID** (one-to-many)

The data covers 500 orders, 336 customers, 3 categories (Electronics, Furniture, Clothing) and 7 payment modes.

## Business Questions

1. How much do we sell and earn, and which months are strongest?
2. Which products make money and which lose it?
3. Who are the top customers, and how many come back?
4. Which divisions and cities sell the most?
5. How do customers pay, and which methods bring the most profit?

## Project Steps

**1. Data cleaning (Power Query)**
- Fixed headers and mixed date formats (`24-01-2025` and `10/3/2025`) into one proper date column
- Set correct data types and trimmed and capitalised text columns
- Checked that Order IDs match between tables

**2. Data model (star schema)**
- Merged both tables into one central **Sales** fact table
- Created lookup tables: **Product**, **Customer**, **Location** and **Calendar** (DAX)
- Connected them with one-to-many, single-direction relationships

**3. DAX measures**
- Total Sales, Total Profit, Profit Margin %, Total Orders, Average Order Value
- Total Customers, Repeat Customers, Repeat Customer %, Sales per Customer
- MoM Sales Growth %, and sales measures for each payment mode

**4. Dashboard design**
- Four pages with synced slicers for Date, Division, Category and Payment Mode

## Dashboard Pages
1) **Executive Overview** Sales Peaked in January and Dipped in June–July · Cash on Delivery Brings in the Most Sales · Electronics Leads Sales, with Clothing Close Behind · Dhaka and Chattogram Drive Over Half of Sales |
2) **Product Performance** Printers Earn the Most Profit of Any Sub-Category · High Sales Don't Always Mean High Profit · Five Sub-Categories Are Losing Money |
3) **Customers and Geography** Our Top 5 Customers by Sales · Only 1 in 3 Customers Buys Again · Dhaka and Chattogram Cities Lead Sales |
4) **Payment Analysis** How Each Division Pays: COD Leads · EMI Customers Spend the Most per Order · COD Makes Up Over a Third of Sales · Credit Card Earns as Much Profit as COD |


## Key Insights

- **613K Taka in sales and 52K Taka in profit**, an 8.44% margin, from 500 orders.
- **January was the best month** (97K Taka); sales dipped in June and July.
- **Electronics sells the most but has the lowest margin (7.9%)**. Clothing earns the most profit and the highest margin (9.2%).
- **Printers are the most profitable sub-category** (12,048 Taka profit).
- **Five sub-categories lose money**: Furnishings, Electronic Games, Three-Piece, Panjabi and Leggings. Electronic Games lost money despite 54,835 Taka in sales.
- **31.85% of customers are repeat buyers**; 68% ordered only once.
- **Dhaka and Chattogram bring in 57% of all sales.**
- **Cash on delivery is the top payment method** (35.5% of sales), but Credit Card earns about the same profit on just over half the sales.

## Limitations

- Only one year of data, so no year-over-year comparison
- No product names, customer IDs, discounts, shipping costs or returns
- Payment mode is recorded per product line, so one order can have several payment methods.

## How to Use

1. Download or clone this repository.
2. Open `E-Commerce Dashboard.pbix` in Power BI Desktop (free).
3. If prompted, point the data source to the CSV files in the `data` folder.

## Author

Sadman Shakib Dipto 
[LinkedIn] (https://www.linkedin.com/in/sadmanshakibdipto/) · [Email](sadipto21@gmail.com)
