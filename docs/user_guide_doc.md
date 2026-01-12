# 📖 Coffee Sales Dashboard User Guide

## Welcome

This comprehensive guide will help you navigate and maximize the value of the Coffee Sales Dashboard. Whether you're an executive reviewing performance, an analyst exploring data patterns, or a team member preparing reports, this guide provides step-by-step instructions for effective dashboard usage.

---

## 🎯 Dashboard Overview

### What This Dashboard Does

The Coffee Sales Dashboard provides interactive visualization of coffee sales performance across multiple dimensions:

- **Time Analysis**: Track sales trends from January 2019 to August 2022
- **Geographic Insights**: Compare performance across United States, Ireland, and United Kingdom
- **Customer Analytics**: Identify top customers and analyze loyalty program impact
- **Product Intelligence**: Understand coffee type, roast, and package size preferences

### Who Should Use This Dashboard

- **Executives**: Strategic decision-making based on high-level trends
- **Sales Managers**: Territory performance tracking and customer relationship management
- **Marketing Teams**: Campaign effectiveness and customer segmentation analysis
- **Operations**: Inventory planning and demand forecasting
- **Finance**: Revenue analysis and profitability assessment

---

## 🚀 Getting Started

### System Requirements

**Minimum Requirements**:
- Microsoft Excel 2016 or later
- Windows 7/macOS 10.12 or newer
- 4 GB RAM
- 50 MB available storage

**Recommended**:
- Microsoft Excel 2019/Microsoft 365
- Windows 10/macOS 11 or newer
- 8 GB RAM or more

**Alternative Software** (with limitations):
- Google Sheets: Upload to Google Drive (some features may not work)
- LibreOffice Calc: Most features compatible, formatting may differ
- Apple Numbers: Partial compatibility

### Installation & Setup

#### Step 1: Download the Dashboard

1. Navigate to the GitHub repository: `https://github.com/enmity101/coffee-sales-dashboard`
2. Click the green **"Code"** button
3. Select **"Download ZIP"** or clone using Git:
   ```bash
   git clone https://github.com/enmity101/coffee-sales-dashboard.git
   ```
4. Extract the ZIP file to your desired location

#### Step 2: Open the Dashboard

1. Navigate to the `dashboard/` folder
2. Double-click **`Coffee_Sales_Dashboard.xlsx`**
3. Excel will open the file

#### Step 3: Enable Content (If Prompted)

If you see a yellow security banner:
1. Click **"Enable Content"** or **"Enable Editing"**
2. This allows slicers and pivot tables to function properly

**Security Note**: This dashboard contains no macros or harmful code. The warning is standard for files downloaded from the internet.

#### Step 4: Navigate to the Dashboard Sheet

1. Look at the sheet tabs at the bottom of Excel
2. Click on the **"Dashboard"** tab
3. You should see the main visualization interface

---

## 📊 Dashboard Layout

### Main Components

```
┌─────────────────────────────────────────────────────────┐
│                 COFFEE SALES DASHBOARD                   │
│                    January 2019 - August 2022           │
├────────────────────────────────┬────────────────────────┤
│  Sales Over Time               │   Interactive Filters  │
│  (Line Chart)                  │                        │
│                                │   □ Order Date         │
│  [Chart showing trends]        │   □ Roast Type         │
│                                │   □ Size               │
│                                │   □ Loyalty Card       │
├────────────────────────────────┴────────────────────────┤
│  Sales by Country              │   Top 5 Customers      │
│  (Column Chart)                │   (Horizontal Bar)     │
│                                │                        │
│  [US | Ireland | UK]           │   [Customer rankings]  │
└─────────────────────────────────────────────────────────┘
```

### Component Descriptions

#### 1. Sales Over Time (Top Left)
**Purpose**: Visualize revenue trends across the entire date range  
**Chart Type**: Multi-line chart  
**What It Shows**:
- Total sales by month (X-axis: Date, Y-axis: Sales $)
- Separate line for each coffee type (Arabica, Excelsa, Liberica, Robusta)
- Trend patterns, seasonality, growth rates

#### 2. Sales by Country (Bottom Left)
**Purpose**: Compare total revenue across three markets  
**Chart Type**: Column/bar chart  
**What It Shows**:
- Total sales per country (United States, Ireland, United Kingdom)
- Sorted from highest to lowest revenue
- Geographic distribution of business

#### 3. Top 5 Customers (Bottom Right)
**Purpose**: Identify highest-value customers  
**Chart Type**: Horizontal bar chart  
**What It Shows**:
- Five customers with greatest total sales
- Customer names (anonymized if needed)
- Revenue contribution per customer

#### 4. Interactive Filters (Top Right)
**Purpose**: Slice data dynamically for focused analysis  
**Filter Types**:
- **Order Date**: Timeline slider
- **Roast Type**: Multi-select (Light, Medium, Dark)
- **Size**: Multi-select (0.2kg, 0.5kg, 1.0kg, 2.5kg)
- **Loyalty Card**: Binary selection (Yes, No)

---

## 🎛️ Using Interactive Filters

Filters (called "Slicers" in Excel) allow you to focus on specific segments without modifying the underlying data.

### Filter Panel Location

The filter panel is located on the right side of the dashboard, above the Top 5 Customers chart.

### How to Apply Filters

#### Order Date Filter (Timeline)

**Purpose**: Analyze specific time periods

**Instructions**:
1. Locate the timeline slicer (horizontal bar with months)
2. **Single Month**: Click on one month
3. **Date Range**: Click and drag across multiple months
4. **Specific Period**: 
   - Click the dropdown arrow on the timeline
   - Select: "Months", "Quarters", or "Years"
   - Choose desired granularity

**Examples**:
- View Q4 2021 performance: Drag from October 2021 to December 2021
- Compare 2020 vs 2021: Use dropdown to select "Years", click 2020, then 2021
- Holiday season analysis: Select Nov-Dec across all years

**Reset**: Click the filter icon (funnel) in the top-right corner of the timeline and select "Clear Filter"

#### Roast Type Filter

**Purpose**: Compare Light, Medium, and Dark roast performance

**Instructions**:
1. Locate the "Roast Type" slicer (three buttons)
2. **Select One**: Click on "Light", "Medium", or "Dark"
3. **Select Multiple**: 
   - Hold **Ctrl** (Windows) or **Cmd** (Mac)
   - Click multiple roast types
4. **Select All**: Click the box in the header

**Use Cases**:
- Isolate medium roast sales trends
- Compare light vs. dark roast in UK market
- Analyze premium (dark) roast customer profiles

**Visual Indicator**: Selected items appear highlighted/pressed

#### Size Filter

**Purpose**: Analyze package size preferences

**Instructions**:
1. Locate the "Size" slicer (four buttons: 0.2, 0.5, 1.0, 2.5)
2. Click on one or multiple sizes (same method as Roast Type)
3. All charts update to show only selected sizes

**Use Cases**:
- Identify which customers buy bulk (2.5kg)
- Track small package (0.2kg) new customer conversions
- Optimize inventory for popular sizes

**Tips**:
- Compare 1.0kg vs. 2.5kg to understand bulk buying behavior
- Filter by 0.2kg + loyalty card to assess sampling program effectiveness

#### Loyalty Card Filter

**Purpose**: Compare loyalty program members vs. non-members

**Instructions**:
1. Locate the "Loyalty Card" slicer (two buttons: Yes, No)
2. Click "Yes" to see only cardholders
3. Click "No" to see non-members
4. Click both to see all customers (default)

**Use Cases**:
- Calculate loyalty program revenue contribution
- Identify top customers without loyalty cards (conversion opportunity)
- Measure loyalty member order frequency

**Key Metric**: Compare average order value between "Yes" and "No" groups

### Combining Multiple Filters

**Power User Technique**: Stack filters for deep-dive analysis

**Example Scenarios**:

1. **Q4 US Dark Roast Performance**:
   - Timeline: Oct-Dec 2021
   - Roast Type: Dark
   - (Geographic filter not available, but note from chart)

2. **Loyalty Member Large Package Buyers**:
   - Loyalty Card: Yes
   - Size: 2.5kg
   - *Result*: See which coffee types this segment prefers

3. **Small Package Non-Member Analysis**:
   - Loyalty Card: No
   - Size: 0.2kg, 0.5kg
   - *Purpose*: Identify trial/sampling customers for conversion

### Clearing Filters

**Reset Individual Filter**:
1. Click the filter icon (funnel) in the top-right corner of slicer
2. Select "Clear Filter from [Filter Name]"

**Reset All Filters**:
1. Go to **Data** tab in Excel ribbon
2. Click **Clear** → **Clear Slicers**
3. All filters return to default (all items selected)

**Quick Reset**: Close and reopen the file (filters reset to default)

---

## 📈 Interpreting Charts & Data

### Reading the Sales Over Time Chart

#### Understanding the Lines

Each colored line represents a coffee type:
- **Line 1** (Brown): Arabica
- **Line 2** (Medium Brown): Excelsa
- **Line 3** (Light Brown): Liberica
- **Line 4** (Dark Brown): Robusta

*(Colors may vary based on your dashboard version)*

#### What to Look For

**Upward Trends**: 
- Consistent growth indicates healthy demand
- Steep increases suggest successful campaigns or seasonality

**Downward Trends**:
- Declining lines may indicate market saturation or competition
- Temporary dips normal for seasonal products

**Seasonality Patterns**:
- Repeating peaks/troughs suggest predictable demand cycles
- Example: Holiday spikes in Q4 (Oct-Dec)

**Crossover Points**:
- When lines cross, one coffee type overtakes another
- Indicates shifting customer preferences

#### Example Analysis

*"Arabica (brown line) shows steady growth from 2019-2021, with peak sales in Q4 2021. Excelsa (medium brown) exhibits the steepest growth curve, suggesting increasing popularity. Notice the dip across all types in summer 2020—likely COVID-19 impact."*

### Reading the Sales by Country Chart

#### Understanding the Bars

Each vertical bar represents total sales for one country:
- **Bar 1** (Tallest): United States
- **Bar 2** (Middle): Ireland
- **Bar 3** (Shortest): United Kingdom

#### What to Look For

**Relative Heights**:
- Taller bars = higher revenue markets
- Compare proportions to understand market distribution

**Gap Analysis**:
- Large gaps suggest opportunity for growth in smaller markets
- Similar heights indicate balanced geographic portfolio

**Changes Over Time**:
- Use date filter to see how country rankings shift
- Example: Compare 2019 vs. 2022 to track UK growth

#### Example Analysis

*"United States generates approximately 50% of total revenue ($17,500), followed by Ireland at 31% ($11,000). United Kingdom represents significant growth opportunity at only 19% market share ($6,500)."*

### Reading the Top 5 Customers Chart

#### Understanding the Horizontal Bars

Each bar represents one customer's total sales:
- **Customer names** appear on the Y-axis (left side)
- **Sales values** shown on the X-axis (bottom)
- **Bars sorted** from highest to lowest (top to bottom)

#### What to Look For

**Customer Concentration**:
- If top customer represents >20% of total sales: High concentration risk
- More balanced bars: Healthier, diversified customer base

**Revenue Gaps**:
- Large gap between #1 and #2 suggests over-reliance on single customer
- Relatively equal bars indicate diverse high-value segment

**Loyalty Status** (requires filter cross-check):
- Apply Loyalty Card: Yes filter
- Check if top 5 changes → measures loyalty program effectiveness

#### Example Analysis

*"Top 5 customers contribute $8,500 (24% of total revenue). Customer A leads at $2,100, followed by Customer B at $1,850. The relatively balanced distribution (within $800 range) indicates moderate concentration risk."*

---

## 🔍 Common Analysis Workflows

### Workflow 1: Monthly Performance Review

**Objective**: Assess current month's performance vs. historical trends

**Steps**:
1. Open dashboard with all filters cleared (default view)
2. Note current month's total sales from "Sales Over Time" chart
3. Apply timeline filter to same month last year
4. Compare year-over-year performance
5. Identify which coffee type drove growth/decline

**Questions to Answer**:
- Are we ahead or behind last year?
- Which coffee type is trending up/down?
- Which country shows strongest momentum?

### Workflow 2: Loyalty Program Impact Assessment

**Objective**: Quantify loyalty program's revenue contribution

**Steps**:
1. Clear all filters (default view)
2. Note total sales from any chart
3. Apply **Loyalty Card: Yes** filter
4. Note new total sales (loyalty member revenue)
5. Calculate: (Loyalty Revenue ÷ Total Revenue) × 100 = Loyalty %
6. Repeat with **Loyalty Card: No** to get non-member revenue

**Questions to Answer**:
- What percentage of revenue comes from loyalty members?
- Are top 5 customers mostly loyalty members?
- How does loyalty member spend compare to non-members?

### Workflow 3: Product Mix Optimization

**Objective**: Identify best-selling product combinations

**Steps**:
1. Clear all filters
2. Apply **Roast Type: Medium** filter
3. Observe which coffee types dominate (Sales Over Time chart)
4. Repeat for **Roast Type: Dark** and **Roast Type: Light**
5. Cross-reference with **Size** filters (0.2kg, 0.5kg, 1.0kg, 2.5kg)

**Questions to Answer**:
- Which roast type generates most revenue?
- Do certain coffee types pair better with specific roasts?
- Are larger packages more popular with specific roast preferences?

### Workflow 4: Geographic Expansion Planning

**Objective**: Evaluate market potential and prioritize growth markets

**Steps**:
1. Note current sales distribution from "Sales by Country" chart
2. Apply **Loyalty Card: Yes** filter
3. Observe if loyalty penetration differs by country (review Top 5 customer locations)
4. Clear loyalty filter, apply timeline to recent 6 months
5. Compare recent trends vs. historical for each country

**Questions to Answer**:
- Which country has lowest penetration (highest growth potential)?
- Are loyalty programs equally effective across geographies?
- Which country shows strongest recent momentum?

### Workflow 5: Customer Retention Analysis

**Objective**: Identify at-risk high-value customers

**Steps**:
1. Clear all filters
2. Note Top 5 Customers from chart
3. Apply timeline filter to last 6 months
4. Check if Top 5 list remains same
5. If customer dropped out: flag for retention campaign

**Questions to Answer**:
- Are top customers consistently ordering?
- Which high-value customers haven't purchased recently?
- Do top customers have loyalty cards? (apply filter to verify)

---

## 💡 Pro Tips & Best Practices

### Data Exploration Tips

**1. Start Broad, Then Narrow**:
- Begin with full dataset (all filters off)
- Observe overall patterns
- Apply filters progressively to drill down

**2. Use Filters in Combination**:
- Don't rely on single filters
- Stack filters for powerful insights
- Example: "Loyalty members + 2.5kg + Dark roast" = super-premium segment

**3. Compare Time Periods Consistently**:
- Use same date ranges for fair comparisons
- Account for seasonality (compare Q4 2021 vs Q4 2020, not Q4 2021 vs Q2 2021)

**4. Cross-Reference Charts**:
- Sales over time shows trends
- Sales by country shows distribution
- Top 5 customers shows concentration
- Together they tell a complete story

### Dashboard Performance Tips

**Keep Excel Responsive**:
- Close other Excel files before opening dashboard
- If slow: Save, close, and reopen file
- Avoid excessive filter clicking (wait for charts to update)

**Prevent Accidental Changes**:
- Dashboard is view-only; source data is protected
- If you want to experiment: Save a copy first (File → Save As)

**Regular Refresh** (if data updates):
- Go to **Data** tab → **Refresh All**
- This recalculates pivot tables and charts
- Only needed if underlying data changes

### Presentation Tips

**Exporting Charts for Reports**:
1. Right-click on any chart
2. Select **"Save as Picture"**
3. Choose format (PNG recommended for quality)
4. Insert into PowerPoint, Word, or email

**Creating Screenshots**:
- Windows: **Win + Shift + S** (Snipping Tool)
- Mac: **Cmd + Shift + 4** (Screenshot tool)
- Capture full dashboard or individual charts

**Printing the Dashboard**:
1. Go to **File** → **Print**
2. Select **"Print Active Sheets"**
3. Adjust **Page Setup** for landscape orientation
4. Scale to fit one page: **Page Setup** → **Scaling** → **Fit to: 1 page wide x 1 page tall**

---

## 🛠️ Troubleshooting

### Common Issues & Solutions

#### Issue: Charts Not Updating When Filters Applied

**Symptoms**: Slicers clicked but charts don't change

**Solutions**:
1. **Check Report Connections**:
   - Right-click slicer → **Report Connections**
   - Ensure all pivot tables are checked
   
2. **Refresh Pivot Tables**:
   - Go to **Data** tab → **Refresh All**
   
3. **Excel Calculation Mode**:
   - **File** → **Options** → **Formulas**
   - Set to **"Automatic"** (not Manual)

#### Issue: Dashboard Looks Different Than Expected

**Symptoms**: Layout broken, charts missing, odd formatting

**Solutions**:
1. **Excel Version Compatibility**:
   - Ensure you're using Excel 2016 or later
   - Update Excel to latest version
   
2. **Enable Content**:
   - Click yellow banner → **Enable Content**
   
3. **Reset Zoom**:
   - Bottom-right corner of Excel
   - Set zoom to **100%** for intended view

#### Issue: Slicers Show No Data

**Symptoms**: Filter buttons empty or show "No data"

**Solutions**:
1. **Clear All Filters First**:
   - Data tab → Clear → Clear Slicers
   
2. **Check Source Data**:
   - Navigate to data sheets (Orders, Customers, Products tabs)
   - Verify data is present
   
3. **Refresh Data**:
   - Data tab → Refresh All

#### Issue: Top 5 Customers Shows Different Names

**Symptoms**: Customer list changes unexpectedly

**Solutions**:
- **This is expected behavior** when filters are applied
- Example: Applying "Loyalty Card: Yes" shows top 5 *loyalty members*, not overall top 5
- Clear filters to see original Top 5

#### Issue: File Won't Open

**Symptoms**: Error message when double-clicking file

**Solutions**:
1. **Unblock File**:
   - Right-click file → **Properties**
   - Check **"Unblock"** box → **Apply** → **OK**
   
2. **Check File Extension**:
   - Must be `.xlsx` (not `.xls` or `.csv`)
   
3. **Reinstall Excel** (last resort)

### Getting Help

**Internal Resources**:
- Review **methodology.md** for technical details
- Check **insights.md** for business context
- Refer to **data_dictionary.md** for field definitions

**External Resources**:
- Microsoft Excel Help: Press **F1** in Excel
- GitHub Issues: Report bugs at repository URL
- Contact dashboard creator: [Your Email]

---

## 📚 Advanced Features

### Custom Filtering (Advanced Users)

**Manual Filter Adjustment**:
1. Right-click any chart → **Filter** → **Value Filters**
2. Set custom thresholds (e.g., "Show only sales > $500")
3. Apply advanced date filters (e.g., "Last 90 days")

**Pivot Table Direct Manipulation**:
1. Right-click chart → **Show Data**
2. Access underlying pivot table
3. Add fields, change aggregations, customize layout
4. Return to Dashboard tab to see changes

### Data Drill-Down

**View Detailed Transactions**:
1. Double-click any data point in a chart
2. Excel opens new sheet with filtered raw data
3. Example: Click top customer bar → see all their orders

**Create Custom Views**:
1. Navigate to **"Orders"** data tab
2. Apply Excel's built-in filters (Data → Filter)
3. Sort, filter, and export subsets as needed

### Exporting Data

**Export Filtered Data**:
1. Apply desired filters on Dashboard
2. Navigate to underlying data tab (Orders)
3. **File** → **Save As** → **CSV** (saves visible data only)

**Export Chart Data**:
1. Right-click chart → **Select Data**
2. Copy series data to new worksheet
3. Use for external analysis (Python, R, etc.)

---

## 📞 Support & Feedback

### Reporting Issues

If you encounter bugs or have questions:

**GitHub Issues** (Preferred):
1. Visit repository: `https://github.com/enmity101/coffee-sales-dashboard`
2. Click **"Issues"** tab
3. Click **"New Issue"**
4. Describe problem with screenshot

**Email Support**:
- Send to: [harshpratapsingh892@gmail.com]
- Include: Excel version, screenshot of issue, steps to reproduce

### Feature Requests

Have ideas for dashboard improvements?

**Submit Enhancement Request**:
1. GitHub Issues → New Issue
2. Tag as "enhancement"
3. Describe desired feature and use case

**Commonly Requested Features**:
- Additional time period comparisons
- Automated report generation
- Integration with live data sources
- Mobile-friendly version

### Contributing

Interested in improving the dashboard?

1. Fork repository on GitHub
2. Make improvements in your copy
3. Submit Pull Request with description
4. Your changes will be reviewed and potentially merged

---

## 📖 Glossary

**Common Terms**:

- **Pivot Table**: Excel tool for summarizing and analyzing large datasets
- **Slicer**: Visual filter that controls multiple charts simultaneously
- **KPI**: Key Performance Indicator, metric measuring business success
- **YoY**: Year-over-Year comparison (e.g., 2021 vs. 2020)
- **CLV**: Customer Lifetime Value, total revenue from a customer over time
- **SKU**: Stock Keeping Unit, unique product identifier

**Dashboard-Specific Terms**:

- **Coffee Type**: Bean variety (Arabica, Excelsa, Liberica, Robusta)
- **Roast Type**: Roasting level (Light, Medium, Dark)
- **Size**: Package weight in kilograms (0.2, 0.5, 1.0, 2.5)
- **Loyalty Card**: Customer enrollment in rewards program (Yes/No)

---

## ✅ Quick Reference Checklist

### Daily Dashboard Check
- [ ] Open dashboard (File → Recent or from saved location)
- [ ] Verify all charts load correctly
- [ ] Clear filters to see full dataset (default view)
- [ ] Note current month's sales trend
- [ ] Check if top 5 customers list changed

### Weekly Analysis
- [ ] Apply date filter to last 7 days
- [ ] Compare to same week last year
- [ ] Review each coffee type performance
- [ ] Identify any unusual spikes/drops
- [ ] Screenshot key charts for team meeting

### Monthly Business Review
- [ ] Generate full month view (timeline filter)
- [ ] Calculate month-over-month growth rate
- [ ] Assess each country's performance
- [ ] Review top 5 customers for churn risk
- [ ] Export charts for presentation
- [ ] Document insights in meeting notes

---

## 🎓 Training Resources

**Recommended Learning Path**:

1. **Beginner** (Week 1):
   - Read this user guide thoroughly
   - Practice applying each filter individually
   - Complete Workflow 1 (Monthly Performance Review)

2. **Intermediate** (Week 2-3):
   - Combine multiple filters for deeper analysis
   - Complete all 5 common workflows
   - Export charts and create summary report

3. **Advanced** (Month 2+):
   - Explore pivot table customization
   - Drill down into raw data
   - Develop custom analysis workflows for your role

**Additional Resources**:
- Microsoft Excel Pivot Table Tutorial: [https://support.microsoft.com/excel](https://support.microsoft.com/excel)
- Data Visualization Best Practices: Tufte, "The Visual Display of Quantitative Information"
- Dashboard repository: `https://github.com/enmity101/coffee-sales-dashboard`

---

## 📅 Document Information

**Version**: 1.0  
**Last Updated**: January 2025  
**Dashboard Version Compatibility**: v1.0.0  
**Author**: Harsh Pratap Singh 
**Contact**: harshpratapsingh892@gmail.com 
**License**: MIT License

---

**Happy Analyzing! ☕📊**

*For technical questions, refer to methodology.md*  
*For business insights, refer to insights.md*  
*For field definitions, refer to data/data_dictionary.md*