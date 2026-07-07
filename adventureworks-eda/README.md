# AdventureWorks Internet Sales — Exploratory Data Analysis

A classic **data analytics EDA project** (Jupyter Notebook) analysing Microsoft's
**AdventureWorks** internet sales data. This is the Python EDA companion to the
original **SQL + Power BI** portfolio project — same dataset, analysed and
visualised with pandas, matplotlib and seaborn.

## 📓 What's inside

```
adventureworks-eda/
├─ AdventureWorks_Sales_EDA.ipynb   # the main notebook (run this)
├─ data/
│   ├─ DimCustomer.csv               # customer dimension
│   ├─ DimDate.csv                   # date dimension
│   ├─ DimProduct.csv                # product dimension
│   ├─ FactInternetSales.csv         # sales fact table
│   ├─ SalesBudget.xlsx              # monthly sales budget
│   └─ original_sql_queries.sql      # the SQL used to clean/export the CSVs
├─ requirements.txt
└─ README.md
```

## 🔎 What it covers

A standard end-to-end analysis workflow:

1. **Business understanding** — the questions we want to answer
2. **Data loading** — the 4 CSVs (no headers) + the Excel budget
3. **Data inspection** — structure, dtypes, summary stats, missing values
4. **Data cleaning & preparation** — date parsing, tidying product attributes,
   and **joining the star schema** (fact + date + customer + product) into one
   analysis-ready `sales` table
5. **Exploratory Data Analysis**
   - Sales Overview (trend, actual vs budget, by year/quarter/weekday)
   - Sales by Customer (top customers, gender, cities, spend distribution)
   - Sales by Product (category, subcategory, top products, colour, line)
   - Order Fulfilment (order-to-ship lead time)
6. **Key insights** (computed from the data)
7. **Conclusion & recommendations**
8. **Future work**

Charts use **matplotlib** and **seaborn**: line, bar, barh, pie, histogram.

## ⚙️ How to run

```bash
cd adventureworks-eda
pip install -r requirements.txt
jupyter notebook AdventureWorks_Sales_EDA.ipynb
```

Then in Jupyter: **Kernel → Restart & Run All** to execute every cell top to
bottom. (Also works in VS Code with the Jupyter extension, or in Google Colab —
just upload the `data/` folder too.)

## 🛠 Tech stack

Python · pandas · numpy · matplotlib · seaborn · openpyxl · Jupyter

## 📊 Example insights produced

- Total internet sales and average order value across all orders
- Best-selling month, product category share and top individual product
- Top customers by spend and the male/female split
- How many months actual sales beat the budget
- Average order-to-ship lead time

## 📁 Data note

The CSVs are the cleaned SQL exports (see `original_sql_queries.sql`), so they
have **no header row** — the notebook supplies the correct column names on load
and treats the literal strings `NULL`/`NA` as missing values.
