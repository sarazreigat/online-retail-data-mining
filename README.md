
# Online Retail II: Data Warehouse, Data Mining and Predictive Analytics

![Online Retail II Analytics](ss.png)

An end-to-end analytics project on 779,425 transactions from a UK online giftware wholesaler (December 2009 to December 2011). The data was cleaned and validated, modelled as a star-schema data warehouse in DuckDB, and analysed with data mining and machine learning. The dataset covers GBP 17.4M of revenue across 41 countries. The analysis found that 19% of customers (the Champions segment) produce 72% of revenue, discovered 510 product association rules with lift up to 56, and predicts which customers will buy next month with a ROC-AUC of 0.80. Monthly revenue shows a strong seasonal pattern that peaks every November.

**Author:** Sara Mohammad Zreigat

## Project files

| File | Description |
|---|---|
| `01_Data_Quality_and_EDA.ipynb` | ETL rules, automated data-quality checks and exploratory analysis |
| `02_Data_Warehouse_Star_Schema.ipynb` | Star schema design, DuckDB warehouse, seven analytical SQL queries, cohort retention |
| `03_Market_Basket_and_Customer_Segmentation.ipynb` | Apriori association rules and RFM + K-Means customer segmentation |
| `04_Predictive_Modeling.ipynb` | Next-month purchase classification and spend regression with time-based evaluation |
| `Online_Retail_Dashboard.html` | Seven-page interactive dashboard; download it and open it in any web browser |
| `Online_Retail_Data_Mining_Report.docx` | Full technical report |
| `Online_Retail_Data_Mining_Presentation.pptx` | Presentation slides |
| `Online_Retail_II_Cleaned.zip` | Cleaned dataset (779,425 rows, 15 columns), compressed CSV |

## Key results

| Area | Result |
|---|---|
| Data quality | 779,425 invoice lines, 36,969 orders, 5,878 customers, GBP 17.37M revenue; 10 of 10 quality checks pass |
| Data warehouse | 1 fact table and 4 dimensions in DuckDB; every analytical query runs in under 0.2 seconds |
| Market basket | 510 association rules; the strongest product pairs reach lift 56 and confidence 89% |
| Segmentation | 4 segments; Champions are 19% of customers and generate 72% of revenue |
| Purchase prediction | Gradient Boosting: F1 0.526 and ROC-AUC 0.800 on five unseen months (naive rule F1 0.421) |
| Spend prediction | Random Forest: MAE GBP 387 and R-squared 0.47 (baseline R-squared 0.16) |

## How to run the notebooks

1. Open [Google Colab](https://colab.research.google.com) and choose **File > Upload notebook**.
2. Unzip `Online_Retail_II_Cleaned.zip` to get `Online_Retail_II_Cleaned.csv`.
3. Choose **Runtime > Run all** and upload the CSV when the notebook asks for it.

All outputs are already saved inside the notebooks, so they can be read directly on GitHub without running them.

## Tools

Python, pandas, NumPy, DuckDB, SQL, scikit-learn, mlxtend, Matplotlib, Plotly

## Data source

Chen, D. (2019). *Online Retail II* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5CG6D (CC BY 4.0)
