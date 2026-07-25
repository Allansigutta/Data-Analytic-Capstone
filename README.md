# Sales Data Analytics & Net Revenue Prediction Capstone

## 📌 Project Overview
The dataset utilized in this analysis consists of 1,200 simulated transactional retail sales records spanning a three-year period from January 2022 to December 2024. The data captures key operational variables for each transaction, including the transaction date, sales region (North, South, East, West), product category (Electronics, Clothing, Food, Home), units sold, unit price, gross revenue, and applied discount percentage. The objective of this report is to evaluate regional performance, identify structural sales patterns, assess the predictive capability of a supervised machine learning model to forecast net revenue, and provide actionable, data-driven recommendations to maximize future profitability.

---

## 📁 Repository Structure
* `capstone_project.ipynb` — Complete Google Colab Jupyter Notebook containing data cleaning, visualisations, model training, and evaluation.
* `Capstone_Project_data.csv` — Sales dataset used for the project.
* `README.md` — Project documentation and summary report.

---

## 🛠️ Tools & Libraries Used
* **Python** (Programming language)
* **Pandas** (Data loading, cleaning, and manipulation)
* **NumPy** (Numerical operations)
* **Matplotlib & Seaborn** (Data visualisations)
* **Scikit-learn** (Linear Regression model and evaluation metrics)

---

## 2. Key Findings
* **Regional Sales are Steady and stable ( Chart 1 & Chart 3):** Based on my line chart and box plot, sales performance across all four regions is quite stable. The East and West regions regularly bring in higher total monthly net revenue, but individual transaction sizes look almost identical across all regions.
* **Product Categories Sell Similar Quantities ( Chart 2):** Looking at the bar chart, all four categories (Clothing, Electronics, Food, and Home) average around 200 units sold per transaction. No single product type sells way more volume than the others.
* **Unit Price Drives Revenue, Not Quantity( Chart 4 & Chart 5):** From the scatter plot and correlation heatmap, unit price has a huge positive correlation with net revenue (0.93). On the other hand, the number of units sold has a much lower correlation (0.26). This means setting higher prices brings in far more money than just trying to move more volume.

## 3. Model Performance
To forecast net transaction revenue, a supervised Multiple Linear Regression model was trained using split validation (80% training, 20% testing). The model's predictive accuracy is highly strong, yielding an R-squared (R²) value of 0.9525. In plain business terms, this means that the model successfully explains 95.25% of the variance observed in transaction-level net revenue. 

## 4. Operational & Data Limitations

When analyzing this data to guide business decisions, a few  limitations need to be kept in mind:

* **Missing Customer & Marketing Context:** The dataset tracks transactions, but it doesn't tell us *who* bought the items or *why*. We don't have data on customer demographics, repeat buyers, or marketing spend. Without knowing how much money was spent on advertising in each region, it's hard to tell if the East and West regions performed better because of higher natural demand or because of heavier ad campaigns.
* **No Tracking of Inventory or Stockouts:** The data shows what was actually sold, but it doesn't show missed opportunities. If a store ran out of stock on Electronics or Home goods in a specific month, those potential sales are invisible in this dataset. This means our revenue trends might reflect inventory shortages rather than true customer demand.
* **Aggregated Regional Data hides City-Level Differences:** The data groups performance into broad regions (North, South, East, West) without breaking down specific cities or store locations. A single underperforming branch could be dragging down an otherwise booming region, or one mega-store could be masking poor sales across smaller locations.

## 5. Recommendations for Investors and Management

Based on our findings, here are clear, data-backed steps the company should take to boost profitability:

* **Cut Back on Broad Discounts (Protect Your Margins):** The model showed that higher discount rates heavily penalize net revenue, while unit price is the main factor driving total sales income. Since customers are buying roughly the same volume (~200 units per transaction) regardless of category, offering steep discounts isn't driving higher volume—it's just giving away profit. We recommend replacing broad discounts with loyalty rewards or minimum-spend bundles.
* **Prioritize Inventory Supply in the East and West:** The East and West regions consistently lead in overall monthly net revenue contribution. Investors and operations teams should prioritize warehouse stock allocation and logistical support to these regions to prevent stockouts and capture maximum market demand during peak months.
* **Standardize Pricing Across Product Categories:** Because transaction sizes and volumes sold are fairly even across Electronics, Food, Clothing, and Home goods, the company should review its pricing tier structure. Focusing marketing and sales efforts on higher-priced premium items within each category will yield much higher profit gains than trying to push sheer volume on lower-priced items.

---

## 🚀 How to Run the Notebook
1. Clone this repository or download `capstone_project.ipynb` and `Capstone_Project_data.csv`.
2. Open the notebook in **Google Colab** or **Jupyter Notebook**.
3. Upload `Capstone_Project_data.csv` to your environment.
4. Run all cells sequentially (`Runtime > Run all`).
