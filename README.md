# Customer-Churn-Returns-Analysis-SQL-Project
📘 Overview
SQL project analyzing customer churn and returns in an e‑commerce dataset.
Covers data cleaning, transformation, and exploration.

🧩 Tables
customer_churn → customer details, orders, churn status
customer_returns → return transactions and refund amounts

🔄 Key Steps

Cleaning: fixed inconsistent values, imputed missing data, removed outliers
Transformation: renamed columns, created ComplaintReceived & ChurnStatus, dropped old flags
Analysis: queries for churn counts, tenure averages, preferred payment modes, refund details

📊 Example Querysql

SELECT cr.ReturnID, cr.CustomerID, cr.ReturnDate, cr.RefundAmount,
       cc.PreferredPaymentMode, cc.Gender, cc.CityTier,
       cc.SatisfactionScore, cc.ChurnStatus, cc.ComplaintReceived
FROM customer_returns cr
JOIN customer_churn cc
ON cr.CustomerID = cc.CustomerID
WHERE cc.ChurnStatus = 'Churned'
  AND cc.ComplaintReceived = 'Yes';


🛠️ Tools
MySQL Workbench
CSV import/export
GitHub for version control

✨ Author
Deenu – Data Analytics Enthusiast
