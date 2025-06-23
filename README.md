# GAM_Price_Optimization
Cellutonz_GAM_Price _Optimization &amp; Event Analysis
#  Cellutionz Price Elasticity & Optimization

This project analyzes historical sales and pricing data from Cellutionz, a mobile device repair business, to estimate price elasticity and optimize pricing strategies using Python and pyGAM.

##  Project Overview

Cellutionz offers repair services for iPhone devices, including:
- iPhone 14 Pro Max & iPhone 14 Pro screen repairs
- LCD repair
- Battery replacement
- Charging port repair

Each service is offered with either **original** or **aftermarket** parts. This analysis uses weekly sales data across 2024, including special events like:
- **Black Friday**
- **Cyber Monday**
- **Christmas Week**

##  Tools & Libraries
- Python (pandas, numpy, matplotlib, seaborn)
- pyGAM for Generalized Additive Modeling
- Jupyter Notebook

##  Key Features
- Load and explore structured CSV data of weekly sales
- Visualize relationships between price and quantity sold
- Apply pyGAM to model non-linear demand curves
- Estimate **price elasticity of demand**
- Determine optimal prices to maximize revenue

## 📁 Files
- `Cellutionz_Pricing_Data.csv`: Simulated repair service sales data for 2024
- `Cellutionz_Price_Elasticity_Analysis.ipynb`: Main Jupyter notebook for analysis
- `README.md`: Project overview and instructions

##  Future Improvements
- Add cost data to compute **profit-maximizing prices**
- Extend elasticity modeling to all product categories
- Integrate promotional campaign analysis (e.g., bundle pricing)

##  Author
Hamid Id Azzi  
[GitHub Profile](https://github.com/)  
Data Analyst | Economics + Tech Repair Background  


							Beginner-Friendly Explanation
Module 1: Introduction to Price Optimization
What is Price Optimization?
Price optimization uses data to find the best price for products that maximizes revenue or profit while considering customer demand.

Why is it Important?
Helps businesses maximize revenue without losing customers.

Identifies price sensitivity (how much demand changes with price).

Helps set competitive prices while maintaining profitability.

Module 2: Data Preparation & Exploration
Step 1: Loading & Cleaning Data
Data Source: A spreadsheet (CSV) containing:

Price (what customers pay)

Quantity Sold (how many units sold)

Product Type (e.g., iPhone 11 LCD, iPhone 13 LCD)

Events (sales, promotions, etc.)

Cleaning Steps:

Remove missing values (NaN) to avoid errors.

Calculate Revenue (Price × Quantity Sold).

Step 2: Exploratory Data Analysis (EDA)
Scatter Plots (Price vs. Quantity Sold):

Helps see if higher prices reduce sales.

Identifies outliers (unusual data points).

Example: If iPhone 11 LCD sells less when price increases, demand is price-sensitive.

Module 3: Modeling Price-Demand Relationships
Step 3: Event Impact Analysis
Question: Do promotions increase sales?

Method: Compare sales with vs. without promotions.

Result: If sales spike during promotions, discounts work.

Step 4: Generalized Additive Models (GAMs)
What is a GAM?

A flexible model that predicts demand based on price.

Captures nonlinear relationships (e.g., demand drops sharply after a certain price).

Why Use GAMs?

More accurate than simple linear regression.

Can estimate uncertainty (best-case/worst-case demand).

How It Works:

Split data by product (each iPhone model gets its own model).

Train models for different scenarios:

Median demand (most likely sales).

Low demand (2.5% quantile) – worst case.

High demand (97.5% quantile) – best case.

Module 4: Finding the Best Price
Step 5: Revenue Optimization
Goal: Find the price that maximizes revenue (not just sales).

Method:

For each product, predict demand at different prices.

Calculate Revenue = Price × Predicted Demand.

Find the price where revenue is highest.

Example Output:

Product	Best Price	Expected Revenue
iPhone 11 LCD	$224.63	$54,446
iPhone 13 LCD	$212.84	$53,641
Step 6: Visualizing Results
Plot Features:

Gray area: Uncertainty range (95% confidence).

Black dots: Actual sales data.

Red dot: Best price (maximizes revenue).

Blue triangles: High/low demand scenarios.

Key Insight:

If the gray area is wide, demand is unpredictable.

If the curve is steep, small price changes affect sales a lot.

Module 5: Business Decisions
How to Use These Insights?
Set Prices Near the Red Dot (optimal revenue point).

Run Promotions Strategically (if events boost sales).

Adjust Inventory based on demand predictions.

Example Business Impact:
If iPhone 13 LCD’s best price is $212.84, but it’s currently sold at $250, lowering the price could increase revenue.

If iPhone 11 LCD demand is unpredictable (wide gray band), consider bundling it with accessories to stabilize sales.

Final Summary
Load & Clean Data → Remove errors, calculate revenue.

Explore Trends → Plot price vs. sales.

Model Demand → GAMs predict sales at different prices.

Optimize Prices → Find the best price for max revenue.

Visualize & Decide → Use graphs to guide pricing strategy.

Business Benefit:
 1-Higher revenue
 2-Better inventory planning
3- Data-driven pricing (not guesswork)

