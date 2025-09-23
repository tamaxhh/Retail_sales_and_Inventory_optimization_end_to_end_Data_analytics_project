## Vendor sales and Inventory optimization complete end to end Data Analytics Project

This README file provides a comprehensive overview of the **Vendor Sales and Inventory Optimization** project.

### Table of Contents

- [Project Overview](!project-overview)
- [Features](!features)
- [Types of Data Used](https://www.google.com/search?q=%23types-of-data-used)
- [Project Structure](https://www.google.com/search?q=%23project-structure)
- [Getting Started](https://www.google.com/search?q=%23getting-started)
- [Key Insights and Recommendations](https://www.google.com/search?q=%23key-insights-and-recommendations)
- [Contact](https://www.google.com/search?q=%23contact)

---

### Project Overview

This project provides a comprehensive analysis of

**retail sales and inventory** to optimize profitability and improve inventory management. By leveraging data from various sources, it identifies key performance indicators, uncovers business insights, and offers actionable recommendations. The project workflow includes data ingestion, cleaning, feature engineering, exploratory data analysis, and creating interactive visualizations.

---

### Features

- **Automated Data Ingestion:** Scripts to load raw CSV data into a local SQLite database.
- **Data Transformation:** Functions to clean data, handle missing values, and create new features such as **`Gross Profit`**, **`Profit Margin`**, **`Stock Turnover`**, and **`Sales to Purchase Ratio`**.
- **Reporting & Recommendations:** A detailed report summarizing key findings and providing strategic recommendations for improving operational efficiency.
- **Interactive Visualization:** A Power BI dashboard for dynamic data exploration and monitoring of vendor performance metrics.

---

### Types of Data Used

This project utilizes several types of structured data files, which are ingested into an SQLite database for analysis:

- **`begin_inventory.csv`** and **`end_inventory.csv`**: These files track the initial and final inventory levels, which are crucial for calculating inventory turnover.
- **`purchase_prices.csv`**: This file contains a list of products and their corresponding purchase prices.
- **`purchases.csv`**: This file records all purchasing activities, including the quantity and cost of products bought from vendors.
- **`sales.csv`**: This file contains sales transaction data, providing insights into revenue and product demand.
- **`vendor_invoice.csv`**: This file contains invoice data from vendors, which is used to calculate freight costs and other vendor-related expenses.

---

### Project Structure

```python
.
├── data/
│   ├── begin_inventory.csv
│   ├── end_inventory.csv
│   ├── purchase_prices.csv
│   ├── purchases.csv
│   ├── sales.csv
│   └── vendor_invoice.csv
├── notebooks/
│   ├── Vendor Performance Analysis.ipynb
│   └── Exploratory Data Analysis.ipynb
├── reports/
│   └── Vendor Performance Report.pdf
├── vendor_performance.pbix
├── get_vendor_summary.py
└── ingestion_db.py
```

---

### Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook
- Power BI Desktop

### Requirements

Install the necessary Python libraries using `pip`:

```python
pip install pandas sqlalchemy sqlite3 matplotlib seaborn
```

### Usage

1. **Data Ingestion:** Place your raw data files (e.g., CSVs) in a `data/` folder. Run the Bash `ingestion_db.py` script to load them into an SQLite database named `inventory.db`.
    
    ```python
    python ingestion_db.py
    ```
    
2. **Data Processing:** Run the `get_vendor_summary.py` script to create the main `vendor_sales_summary` table with cleaned data and new performance metrics.
    
    ```python
    python get_vendor_summary.py
    ```
    
3. **Exploratory Data Analysis:** Open the Jupyter Notebooks (`Exploratory Data Analysis.ipynb` and `Vendor Performance Analysis.ipynb`) to explore the data and replicate the analysis.
    
    ```python
    jupyter notebook
    ```
    
4. **Reporting and Visualization:** View the detailed findings in `Vendor Performance Report.pdf` and open `vendor_performance.pbix` with Power BI Desktop to interact with the dashboard.

---

### Key Insights and Recommendations

Based on the analysis, the project highlights several key insights:

- **Profitability Variance:** There is a significant difference in profit margins between top-selling and low-performing vendors, confirmed by statistical hypothesis testing.
- **High-Margin vs. High-Volume:** High-margin vendors may benefit from better pricing strategies, while top-selling vendors could focus on improving cost efficiency.

The final report provides strategic recommendations, including:

- Re-evaluating pricing for low-sales, high-margin brands to boost sales volume without sacrificing profitability.
- Diversifying vendor partnerships to reduce dependency on a few suppliers and mitigate supply chain risks.
- Leveraging bulk purchasing advantages to maintain competitive pricing while optimizing inventory management.
- Optimizing slow-moving inventory by adjusting purchase quantities, launching clearance sales, or revising storage strategies.
- Enhancing marketing and distribution strategies for low-performing vendors to drive higher sales volumes without compromising profit margins.

---

### Contact

For any questions or suggestions, please open an issue or contact the project author.
