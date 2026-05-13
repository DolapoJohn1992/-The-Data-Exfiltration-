# Session 25: SQL Injection & Data Exfiltration

## 🎯 Project Mission
This project demonstrates a successful SQL Injection (SQLi) attack against a vulnerable web application to bypass authentication and exfiltrate sensitive employee data.

## 🛠️ Methodology
* **Authentication Bypass:** Utilized a tautology payload (`' OR 1=1 --`) to bypass the login portal without a valid password.
* **Database Mapping:** Leveraged UNION-based SQL injection to discover the database structure, identifying 2 columns in the employees table.
* **Data Exfiltration:** Extracted restricted salary information using a UNION SELECT statement.

## 📊 Findings
* **Target:** Alice (CEO)
* **Extracted Data:** $350,000

## 🛡️ Remediation
The primary defense implemented to prevent this vulnerability is the use of **Parameterized Queries** (Prepared Statements), which ensures the database treats user input as data rather than executable code.
