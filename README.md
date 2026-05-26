# End-to-End Taxi Ride Analytics Pipeline (PostgreSQL × Power BI)
🚀 **Production-Grade BI Architecture with Live Gateway Integration**

👉 **[View my Project Launch Post on LinkedIn](ADD_YOUR_LINKEDIN_POST_URL_HERE)**

<img width="1248" height="697" alt="Screenshot 2026-05-26 191619" src="https://github.com/user-attachments/assets/e178cb96-1a31-4bc6-8129-95ee37179bbf" />
<img width="1247" height="702" alt="Screenshot 2026-05-26 191644" src="https://github.com/user-attachments/assets/ddad1ecc-5698-4b09-9aab-356f0c1ecb36" />
<img width="1248" height="698" alt="Screenshot 2026-05-26 191604" src="https://github.com/user-attachments/assets/b39c032a-c226-437e-a6f0-13e1c1d653c8" />


## 📌 Project Overview
This project showcases an industry-level data analytics pipeline built to handle transactional ride-booking records. Moving completely away from basic flat files (like CSVs or Excel), this architecture implements a dynamic connection between a relational database engine (**PostgreSQL**) and **Power BI Cloud Service** using an **On-Premises Data Gateway** infrastructure.

## 💡 Key Technical Learnings & Breakthroughs
Through this project, I moved past basic dashboard design and mastered production-level data engineering workflows:

1. **Database Connection & Query Methods (PostgreSQL):** * Learned how to hook up an enterprise database directly to Power BI.
   * Explored different data connection modes, specifically implementing **DirectQuery/Mixed Mode** to execute live background SQL query requests straight to the local database instead of relying on static local copies.
2. **Industry-Standard Visual Engineering:** * Learned how professional production dashboards are structured in corporate environments.
   * Mastered advanced user-experience elements including state-driven interactive buttons, horizontal menu distribution, and a clean, dedicated homepage navigation hub to smoothly jump between reporting pages.
3. **Data Gateway Infrastructure & Cloud Publishing:** * Learned how to securely publish local development work to the live web portal (**Power BI Service**).
   * Successfully installed, registered, and configured a Microsoft On-Premises Data Gateway (Standard Mode) to bridge network credentials and securely stream live data from my local machine to the cloud.

## 🛠️ Tech Stack & Components
* **Database Layer:** PostgreSQL (Relational schema modeling, structural constraints, and transactional storage)
* **BI & Visualization Layer:** Power BI Desktop & Power BI Cloud Service
* **Enterprise Bridge:** Microsoft On-Premises Data Gateway (Standard Mode)
* **Data Modeling:** Advanced DAX (Data Analysis Expressions) for customized time-intelligence dimensions

## 📐 Data Schema & Modeling
The analytics framework relies on a production-optimized star schema:
* **Fact Table:** `public.bi_fact_sales` (Capturing live transaction IDs, base booking values, timestamps, and customer/driver keys)
* **Dimension Table:** `DimDate` (Handling chronological layers including precise Date Hierarchies, Quarters, and Custom Month Names)

## 📈 Featured Analytical Expressions (DAX)
Chronological grouping arrays created for dynamic dashboard axis labels:
```dax
Month Name = FORMAT(rideBookings[Date], "MMMM")
