# ☕ Coffee Sales Dashboard

A comprehensive Excel-based analytics dashboard for visualizing and analyzing coffee sales data across multiple dimensions including time, geography, customer segments, and product categories.

<img width="1742" height="826" alt="image" src="https://github.com/user-attachments/assets/02941c5e-af7b-43ba-890e-f0e0f8172b55" />

*Interactive dashboard showcasing sales trends, geographic distribution, and customer analytics*

## 📊 Project Overview

This project provides actionable insights into coffee sales performance from January 2019 to August 2022. The dashboard enables stakeholders to explore sales patterns, identify top-performing products and customers, and make data-driven decisions to optimize business strategy.

### Key Features

- **Time Series Analysis**: Track sales trends over 43+ months across different coffee types
- **Geographic Insights**: Compare sales performance across United States, Ireland, and United Kingdom
- **Customer Analytics**: Identify and analyze top 5 customers by total revenue
- **Interactive Filtering**: Dynamic filters for roast type, package size, and loyalty card status
- **Product Segmentation**: Breakdown by coffee type (Arabica, Excelsa, Liberica, Robusta) and roast level

## 🗂️ Repository Structure

```
coffee-sales-dashboard/
│
├── data/
│   ├── raw/                    # Original source data files
│   ├── processed/              # Cleaned and transformed datasets
│   └── data_dictionary.md      # Detailed field descriptions
│
├── dashboard/
│   └── Coffee_Sales_Dashboard.xlsx    # Main Excel dashboard file
│
├── assets/
│   └── dashboard_preview.png   # Dashboard screenshot
│
├── README.md                   # Project documentation (this file)
└── LICENSE                     # MIT License
```

## 📈 Dashboard Components

### 1. Sales Over Time
Line chart visualizing total sales trends from 2019-2022, segmented by coffee type:
- Arabica
- Excelsa
- Liberica
- Robusta

### 2. Sales by Country
Bar chart comparing total revenue across three markets:
- United States
- Ireland
- United Kingdom

### 3. Top 5 Customers
Horizontal bar chart highlighting highest-revenue customers by total sales value.

### 4. Interactive Filters
- **Roast Type**: Light, Medium, Dark
- **Size**: 0.2 kg, 0.5 kg, 1.0 kg, 2.5 kg
- **Loyalty Card**: Yes/No

## 💾 Dataset Description

### Orders Table
Primary transactional dataset containing sales records.

| Field | Description | Data Type |
|-------|-------------|-----------|
| Order ID | Unique identifier for each order | Text |
| Order Date | Date of order placement | Date |
| Customer ID | Foreign key linking to Customers table | Text |
| Product ID | Foreign key linking to Products table | Text |
| Quantity | Number of units ordered | Integer |
| Customer Name | Full name of customer | Text |
| Email | Customer email address | Text |
| Country | Customer country (US, Ireland, UK) | Text |
| Coffee Type | Type of coffee bean | Text |
| Roast Type | Roasting level | Text |
| Size | Package size in kg | Decimal |
| Unit Price | Price per unit | Currency |
| Sales | Total sales amount (Quantity × Unit Price) | Currency |

### Customers Table
Customer master data for relationship management.

| Field | Description | Data Type |
|-------|-------------|-----------|
| Customer ID | Unique customer identifier | Text |
| Customer Name | Full name | Text |
| Email | Contact email | Text |
| Phone Number | Contact phone | Text |
| Address Line 1 | Street address | Text |
| City | City name | Text |
| Country | Country name | Text |
| Postcode | Postal/ZIP code | Text |
| Loyalty Card | Loyalty program enrollment status | Boolean |

### Products Table
Product catalog with pricing and specifications.

| Field | Description | Data Type |
|-------|-------------|-----------|
| Product ID | Unique product identifier | Text |
| Coffee Type | Bean variety (Arabica, Excelsa, etc.) | Text |
| Roast Type | Light, Medium, or Dark roast | Text |
| Size | Package size in kg | Decimal |
| Unit Price | Selling price per unit | Currency |
| Price per 100g | Normalized price for comparison | Currency |
| Profit | Profit margin per unit | Currency |

## 🚀 Getting Started

### Prerequisites
- Microsoft Excel 2016 or later (or compatible spreadsheet software)
- Basic understanding of pivot tables and Excel functions

### Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/coffee-sales-dashboard.git
cd coffee-sales-dashboard
```

2. Open the dashboard:
```bash
cd dashboard
# Open Coffee_Sales_Dashboard.xlsx in Excel
```

### Usage

1. **Explore the Dashboard**: Navigate to the "Dashboard" sheet to view all visualizations
2. **Apply Filters**: Use the slicers on the right side to filter data by roast type, size, and loyalty card status
3. **Analyze Trends**: Click on chart elements to drill down into specific data points
4. **Export Insights**: Use Excel's built-in export features to save charts as images or PDFs

## 📊 Key Insights

*For detailed analysis and business recommendations, see [docs/insights.md](docs/insights.md)*

- Sales show seasonal patterns with peak periods in [specific months]
- [Country] represents the largest market by total revenue
- Loyalty card holders generate [X]% higher average order value
- [Coffee Type] is the best-selling product category

## 🛠️ Built With

- **Microsoft Excel**: Dashboard creation and data visualization
- **Pivot Tables**: Dynamic data aggregation and analysis
- **Excel Formulas**: VLOOKUP, XLOOKUP, INDEX-MATCH for data integration
- **Slicers**: Interactive filtering mechanism

## 📝 Methodology

The dashboard employs the following data processing steps:

1. **Data Integration**: Merging Orders, Customers, and Products tables using XLOOKUP/VLOOKUP
2. **Data Cleaning**: Removing duplicates, handling missing values, standardizing formats
3. **Calculated Fields**: Computing total sales (Quantity × Unit Price)
4. **Aggregation**: Creating pivot tables for time series and categorical analysis
5. **Visualization**: Building interactive charts with dynamic date ranges

## 🤝 Contributing

Contributions are welcome! If you'd like to improve this dashboard or add new features:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📧 Contact

Your Name - [@harshsingh94](www.linkedin.com/in/harshsingh94) - harshpratapsingh892@gmail.com

Project Link: [https://github.com/enmity101/Coffee-Sales-Dashboard](https://github.com/enmity101/Coffee-Sales-Dashboard)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Dataset inspired by real-world coffee retail operations
- Dashboard design principles from Edward Tufte's data visualization best practices
- Excel techniques learned from the data analytics community

---

**⭐ If you find this project useful, please consider giving it a star!**
