
# Sales Dashboard Project

## Introduction

This project provides an interactive sales dashboard using Microsoft Power BI for data visualization and analysis. The dashboard helps the sales team and management to monitor performance, identify trends, and make data-driven decisions.

## Features

- **Total Revenue Display**
- **Top Customers Analysis**
- **Top Products Analysis**
- **Sales Quantity Display**
- **Revenue Trend Analysis**

## Prerequisites

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/)
- Access to sales data sources(dump is given in the attachments)


## Installation

1. **Clone the Repository:**
   ```sh
   git clone https://github.com/your-username/your-repo-name.git
   ```

2. **Navigate to the Project Directory:**
   ```sh
   cd your-repo-name
   ```

3. **Open the Power BI File:**
   Open the `.pbix` file in Power BI Desktop.

## Usage

1. **Load Data:**
   Connect to your sales data sources and load the data into the Power BI dashboard.

2. **Customize Visualizations:**
   Modify the existing visualizations or add new ones to meet your requirements.

3. **Publish Dashboard:**
   Publish the dashboard to the Power BI Service or share it within your organization.

4. **Interact with the Dashboard:**
   Use filters, slicers, and other interactive elements to explore the data.

## Key Metrics

### Total Revenue

- **Description:** Displays the total revenue generated over a specified period.
- **Calculation:** 
  ```plaintext
  Total Revenue = SUM(Revenue)
  ```

### Top Customers

- **Description:** Shows the top customers based on the revenue they contributed.
- **Fields:** Customer Name, Revenue
- **Query:**
  ```plaintext
  SELECT CustomerName, SUM(Revenue) as TotalRevenue
  FROM SalesData
  GROUP BY CustomerName
  ORDER BY TotalRevenue DESC
  LIMIT 10;
  ```

### Top Products

- **Description:** Shows the top products based on the revenue they generated.
- **Fields:** Product Name, Revenue
- **Query:**
  ```plaintext
  SELECT ProductName, SUM(Revenue) as TotalRevenue
  FROM SalesData
  GROUP BY ProductName
  ORDER BY TotalRevenue DESC
  LIMIT 10;
  ```

### Sales Quantity

- **Description:** Displays the total number of units sold.
- **Calculation:**
  ```plaintext
  Total Sales Quantity = SUM(SalesQuantity)
  ```

### Revenue Trend

- **Description:** A chart showing how revenue changes over time, helping to identify trends and patterns in sales performance.
- **Fields:** SaleDate, Revenue
- **Query:**
  ```plaintext
  SELECT SaleDate, SUM(Revenue) as TotalRevenue
  FROM SalesData
  GROUP BY SaleDate
  ORDER BY SaleDate;
  ```



## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact

Your Name - lingamvarsha58@gmail.com

Project Link: https://github.com/VARSHAlingam123/PowerBI/sales

---

This README file provides a clear and concise overview of the project, its features, installation steps, usage instructions, and key metrics, making it easy for users to understand and use the sales dashboard.
