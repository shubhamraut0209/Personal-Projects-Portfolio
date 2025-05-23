# 🛒 Market Basket Analysis on Online Retail II Dataset

This project explores customer purchase behavior using Market Basket Analysis (MBA) techniques on the **Online Retail II** dataset. Implemented in R, the project identifies frequent itemsets and association rules that can be used to enhance product placement strategies and cross-selling techniques in e-commerce.

## 📌 Objective

- Perform market basket analysis using association rule mining.
- Identify combinations of products frequently bought together.
- Visualize item relationships to derive actionable insights.

## 🧰 Technologies Used

- **Language:** R
- **IDE:** Google Colab via R kernel
- **Libraries:** `arules`, `arulesViz`, `dplyr`, `ggplot2`
- **Dataset Source:** UCI Machine Learning Repository – [Online Retail II](https://archive.ics.uci.edu/ml/datasets/Online+Retail+II)

## 📊 Dataset Overview

- **Region:** United Kingdom
- **Time Period:** 01/12/2009 – 09/12/2011
- **Variables:** InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country
- **Preprocessing Steps:**
  - Removed missing values and duplicates
  - Filtered only positive quantities and UK transactions
  - Created transaction basket by invoice number

## 🔍 Methodology

1. **Data Cleaning and Preparation**
   - Filtered UK data and retained relevant fields
   - Aggregated data by `InvoiceNo` to form transactions

2. **Transaction Conversion**
   - Converted the dataset into a `transactions` class suitable for `arules`

3. **Association Rule Mining**
   - Used the **Apriori algorithm** with varying support and confidence thresholds
   - Analyzed rules with measures such as lift, support, and confidence

4. **Visualization**
   - Visualized item frequency and rules using `arulesViz`

## 📈 Key Insights

- Discovered frequent itemsets such as:
  - `{WHITE HANGING HEART T-LIGHT HOLDER, REGENCY CAKESTAND 3 TIER}`
  - `{JUMBO BAG RED RETROSPOT}` → `{POSTAGE}`
- Lift values greater than 1 indicated strong associations useful for cross-selling.

## 📚 Future Enhancements

- Deploy dashboard using Shiny for interactive exploration
- Extend analysis across other countries (e.g., Germany, France)
- Integrate temporal dimension for seasonal purchasing patterns

## 👤 Author

**Shubham Umesh Raut**  
Data Science Enthusiast | R Programmer  

## 📜 License

This project is open for educational and non-commercial use. Please give proper attribution if reused.
