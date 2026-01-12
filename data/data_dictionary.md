# 📚 Data Dictionary

This document provides comprehensive descriptions of all fields across the three core datasets used in the Coffee Sales Dashboard.

## 📦 Orders Table

The Orders table contains transactional data representing individual coffee sales transactions.

**Record Count**: ~1,000 orders (Jan 2019 - Aug 2022)

| Field Name | Data Type | Format | Description | Example | Constraints |
|------------|-----------|--------|-------------|---------|-------------|
| **Order ID** | Text | Alphanumeric | Unique identifier for each order transaction | `ORD-2019-001` | Primary Key, Not Null |
| **Order Date** | Date | MM/DD/YYYY | Date when the order was placed | `01/15/2019` | Not Null, Range: 01/2019 - 08/2022 |
| **Customer ID** | Text | Alphanumeric | Links to Customers table | `CUST-001` | Foreign Key, Not Null |
| **Product ID** | Text | Alphanumeric | Links to Products table | `PROD-AR-L-02` | Foreign Key, Not Null |
| **Quantity** | Integer | Whole number | Number of units purchased in order | `3` | Positive integer, typically 1-10 |
| **Customer Name** | Text | Free text | Full name of purchasing customer | `John Smith` | Not Null |
| **Email** | Text | Email format | Customer's email address | `john.smith@email.com` | Valid email format |
| **Country** | Text | Country name | Customer's country of residence | `United States` | Limited to: US, Ireland, UK |
| **Coffee Type** | Text | Category | Variety of coffee bean | `Arabica` | Values: Arabica, Excelsa, Liberica, Robusta |
| **Roast Type** | Text | Category | Level of roasting | `Medium` | Values: Light, Medium, Dark |
| **Size** | Decimal | Numeric (kg) | Package weight in kilograms | `0.5` | Values: 0.2, 0.5, 1.0, 2.5 |
| **Unit Price** | Currency | USD | Price per single unit | `$12.99` | Positive decimal |
| **Sales** | Currency | USD | Total revenue (Quantity × Unit Price) | `$38.97` | Calculated field |

### Business Rules
- Each Order ID must be unique
- Order Date must be within the operational period (2019-2022)
- Sales amount is automatically calculated: `Sales = Quantity × Unit Price`
- Customer and Product information is denormalized for dashboard performance

---

## 👥 Customers Table

The Customers table maintains master data for all registered customers.

**Record Count**: ~50 unique customers

| Field Name | Data Type | Format | Description | Example | Constraints |
|------------|-----------|--------|-------------|---------|-------------|
| **Customer ID** | Text | Alphanumeric | Unique customer identifier | `CUST-001` | Primary Key, Not Null |
| **Customer Name** | Text | Free text | Full legal or business name | `Jane Doe` | Not Null |
| **Email** | Text | Email format | Primary contact email | `jane.doe@email.com` | Valid email, Unique |
| **Phone Number** | Text | Phone format | Contact phone number | `+1-555-0123` | International format |
| **Address Line 1** | Text | Free text | Street address | `123 Main Street` | Not Null |
| **City** | Text | City name | City of residence | `New York` | Not Null |
| **Country** | Text | Country name | Country of residence | `United States` | Values: United States, Ireland, United Kingdom |
| **Postcode** | Text | Postal code | ZIP or postal code | `10001` | Format varies by country |
| **Loyalty Card** | Boolean | Yes/No | Loyalty program enrollment | `Yes` | Values: Yes, No |

### Business Rules
- Each customer can have only one Loyalty Card status
- Email must be unique across all customers
- Country must match one of the three supported markets
- Loyalty Card holders may receive special pricing or promotions

---

## 🛍️ Products Table

The Products table catalogs all available coffee products with pricing details.

**Record Count**: ~48 unique products (4 coffee types × 3 roasts × 4 sizes)

| Field Name | Data Type | Format | Description | Example | Constraints |
|------------|-----------|--------|-------------|---------|-------------|
| **Product ID** | Text | Alphanumeric | Unique product SKU | `PROD-AR-M-05` | Primary Key, Not Null |
| **Coffee Type** | Text | Category | Bean variety | `Arabica` | Values: Arabica, Excelsa, Liberica, Robusta |
| **Roast Type** | Text | Category | Roasting level | `Medium` | Values: Light, Medium, Dark |
| **Size** | Decimal | Numeric (kg) | Package weight | `0.5` | Values: 0.2, 0.5, 1.0, 2.5 |
| **Unit Price** | Currency | USD | Retail price per package | `$12.99` | Positive decimal |
| **Price per 100g** | Currency | USD | Normalized price for comparison | `$2.60` | Calculated from Unit Price ÷ (Size × 10) |
| **Profit** | Currency | USD | Profit margin per unit sold | `$3.25` | Positive decimal |

### Business Rules
- Product ID format typically includes coffee type code, roast code, and size code
- Price per 100g enables fair comparison across different package sizes
- Profit represents gross margin before operational expenses
- Larger sizes generally offer better per-gram value to customers

---

## 🔗 Data Relationships

### Entity Relationship Diagram

```
┌─────────────┐         ┌─────────────┐         ┌─────────────┐
│  CUSTOMERS  │         │   ORDERS    │         │  PRODUCTS   │
├─────────────┤         ├─────────────┤         ├─────────────┤
│ Customer ID │◄───────┤ Customer ID │         │ Product ID  │◄───┐
│ Name        │         │ Product ID  │─────────┤ Coffee Type │    │
│ Email       │         │ Order ID    │         │ Roast Type  │    │
│ Country     │         │ Order Date  │         │ Size        │    │
│ Loyalty Card│         │ Quantity    │         │ Unit Price  │    │
└─────────────┘         │ Sales       │         │ Profit      │    │
                        └─────────────┘         └─────────────┘    │
                                                                    │
                                1:N relationship ─────────────────┘
```

### Relationship Types
- **Customers to Orders**: One-to-Many (one customer can place multiple orders)
- **Products to Orders**: One-to-Many (one product can appear in multiple orders)
- **Orders**: Junction/fact table connecting Customers and Products

---

## 📊 Data Quality Notes

### Data Coverage
- **Time Period**: January 2019 to August 2022 (43 months)
- **Geographic Coverage**: 3 countries (United States, Ireland, United Kingdom)
- **Product Range**: 4 coffee types × 3 roast levels × 4 package sizes = 48 SKUs

### Known Limitations
- Some early 2019 orders may have incomplete customer contact information
- Loyalty card program launched mid-2019, so earlier customers may show "No" by default
- Price changes over time are not tracked in the Products table (current prices only)
- International shipping costs not reflected in Sales figures

### Data Freshness
- Last updated: August 2022
- Refresh frequency: Historical dataset (static)
- For current data, refer to live sales systems

---

## 🔍 Common Queries

### Example Analysis Questions This Data Can Answer

1. **Sales Trends**: How have sales evolved over time for each coffee type?
2. **Customer Behavior**: Do loyalty card holders purchase larger quantities?
3. **Geographic Performance**: Which country generates the highest revenue?
4. **Product Mix**: What's the most popular combination of coffee type, roast, and size?
5. **Customer Lifetime Value**: Who are our top 5 customers by total spending?
6. **Pricing Strategy**: Is there correlation between package size and sales volume?
7. **Seasonality**: Are there seasonal patterns in coffee sales?

---

## 📝 Change Log

| Date | Version | Changes |
|------|---------|---------|
| Aug 2022 | 1.0 | Initial dataset compiled from operational systems |
| Jan 2025 | 1.1 | Documentation created for GitHub repository |

---

## 📧 Questions?

If you have questions about the data structure or need clarification on specific fields, please open an issue in the GitHub repository.