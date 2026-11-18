# CRM Sales Dashboard Analytics

An interactive Power BI dashboard for analyzing CRM sales performance, revenue trends, sales-agent productivity, and sector and product performance.

## Overview

The dashboard helps organizations monitor key sales metrics, compare account and regional performance, identify top sales agents, and analyze revenue by sector and product.

## Dashboard Summary

| Metric | Value |
|---|---:|
| Total employees | 396K |
| Total revenue | 363M |
| Win rate | 57.46% |
| Average deal size | 22.99 |
| Total deals closed | 4,238 |

## Key Features

- Sales KPI cards and deal-stage analysis
- Revenue trends over time
- Revenue by account and regional office
- Top 10 accounts and top 10 deals won by sales agent
- Top 5 sales agents by win rate
- Revenue by sector and product
- Interactive filtering by region, sales agent, sector, product, and reporting period

## Repository Structure

```text
CRM_Sale_Dashboard_Analytics/
|-- README.md
|-- requirements.txt
|-- .env.example
|-- .gitignore
|-- assets/
|   |-- crm_project_page-0002.jpg
|   `-- crm_project_page-0003.jpg
|-- dataset/
|   |-- raw/
|   |   |-- sales_teams.csv
|   |   |-- products.csv
|   |   `-- data_dictionary.csv
|   `-- processed/
|       |-- Accounts_cleaned.csv
|       `-- Sales_pipeline_cleaned.csv
|-- notebooks/
|   |-- Data_Cleaning.ipynb
|   `-- Database_Connection.ipynb
`-- powerbi/
    `-- crm_sales_dashboard.pbix
```

## Tech Stack

- Power BI Desktop
- Python
- Pandas
- Jupyter Notebook
- Scikit-learn
- SQLAlchemy and PyMySQL
- MySQL

## Prerequisites

- Power BI Desktop
- Python 3.9 or later
- Jupyter Notebook or JupyterLab
- A MySQL database for database integration

Install Python dependencies:

```bash
pip install -r requirements.txt
```

## Database Configuration

Copy `.env.example` to `.env`, then add the local database credentials:

```text
DB_USERNAME=root
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=3306
DB_DATABASE=crm_sales_db
```

Do not commit `.env` or real database passwords to GitHub.

## How to Run

### 1. Prepare the data

1. Open `notebooks/Data_Cleaning.ipynb`.
2. Run the notebook cells to clean and transform the source data.
3. Store generated datasets in `data/processed/`.

### 2. Upload data to MySQL

1. Configure the values in `.env`.
2. Open `notebooks/Database_Connection.ipynb`.
3. Run all cells to upload the processed and reference datasets to MySQL.

### 3. Open the dashboard

1. Open `powerbi/crm_sales_dashboard.pbix` in Power BI Desktop.
2. Configure or refresh the database connection.
3. Use the dashboard filters to explore the sales data.

## Using the Dashboard

Filter and analyze data by:

- Regional office
- Sales agent
- Product
- Sector
- Reporting period

## Data Files

| Path | Description |
|---|---|
| `dataset/raw/sales_teams.csv` | Sales-team and regional-office data |
| `dataset/raw/products.csv` | Product and category data |
| `dataset/raw/data_dictionary.csv` | Source-field definitions |
| `dataset/processed/Accounts_cleaned.csv` | Cleaned account data |
| `dataset/processed/Sales_pipeline_cleaned.csv` | Cleaned sales-pipeline data |
