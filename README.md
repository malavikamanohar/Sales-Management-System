# Sales Management System

## Overview
The Sales Management System is a web-based application designed to help businesses efficiently manage and track their sales activities. The app allows users to record sales transactions, manage products, view sales reports, and monitor the performance of sales representatives. It provides an intuitive interface to track daily, monthly, and yearly sales data, helping businesses make informed decisions and improve their sales processes.

## Features
- **Home**: Welcome page with an overview of the Sales Management System.
- **Sales**: Allows users to log sales transactions, including product details, quantity, price, and customer information.
- **Products**: Manage product catalog by adding, updating, or removing products.
- **Reports**: Displays detailed sales performance reports and analytics, including total sales, sales by product, and sales by representative.
- **Dashboard**: Visualizes sales data, product performance, and sales representative performance over time.
- **User Management**: Allows managers to add and manage sales representatives, assign them territories, and track their performance.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/sales-management-system.git
    cd sales-management-system
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Ensure you have the database and model files in the correct directories:
    - `./data/sales_data.csv` - Sales transaction data file.
    - `./models/sales_model.pkl` - Pre-trained machine learning model for sales prediction.

4. Make sure the `up.sh` script is executable:
    ```bash
    chmod +x up.sh
    ```

## Usage

1. Start the application:
    ```bash
    streamlit run app.py
    ```

2. Open your browser and navigate to [http://localhost:8501](http://localhost:8501) to access the app.

## App Structure

### 1. Home
- Displays a welcome message and an overview of the Sales Management System.
- Option to navigate to various sections of the app (Sales, Products, Reports, etc.).

### 2. Sales
- Users can input sales data such as product ID, quantity, price, and customer information.
- Sales transactions are logged, and the app displays a summary of the transaction.

### 3. Products
- Allows users to manage the product catalog.
- Users can add new products, update existing products, or remove products from the catalog.
- Each product has details like product name, description, price, and available stock.

### 4. Reports
- Provides various reports, such as:
  - **Sales by product**: Total sales for each product.
  - **Sales by representative**: Total sales for each sales representative.
  - **Sales over time**: Visualizing sales trends by month, quarter, or year.
- A detailed analysis is provided with graphs and tables to understand sales performance.

### 5. Dashboard
- Offers a set of visualizations for analyzing sales data:
  - **Sales volume over time**: A time series graph of sales across different periods.
  - **Top-selling products**: A bar chart of products with the highest sales.
  - **Sales by region**: A map showing sales performance across different territories.
  - **Sales representative performance**: A leaderboard showing the performance of individual sales representatives.

### 6. User Management
- Admin users can add and manage sales representatives.
- Sales reps are assigned specific territories or regions.
- Admins can track and evaluate the performance of sales reps.

## Data Preparation

The data is loaded from `./data/sales_data.csv`.

- The dataset contains columns like `Date`, `ProductID`, `Quantity`, `Price`, `CustomerID`, `SalesRepID`.
- The `Date` column is converted to a datetime format.
- Additional columns like `Year`, `Month`, `Day`, `Quarter`, and `DayOfWeek` are created for easier analysis.

## Product Mapping

A dictionary is used to map numeric product IDs to their corresponding product names:

```python
product_mapping = {
    101: 'Product A',
    102: 'Product B',
    103: 'Product C',
    104: 'Product D'
}
