# Automotive Sales Performance Analysis & Dashboard (2025)

## 📌 Executive Summary
This project delivers an end-to-end Automotive Sales Performance Analytics solution. By processing over 10,000 corporate transaction records covering the fiscal year 2025, this project bridges programmatic data engineering with corporate business intelligence. The findings uncover localized branch contributions, consumer segment dynamics, car model yields, and financing distribution to drive strategic decisions in inventory management and sales operations.

Note: Graha Auto Nusantara is a fictional company name used purely for this data analysis simulation. Dataset provided by KarirNex.

## 🚀 Key Business Questions Addressed
1. What is the dealership's high-level sales matrix (Gross revenue, transaction velocity, total quantity, and fulfillment completion)?
2. Which vehicle categories (SUV, MPV, Hatchback, Pickup, or EV) and specific models generate the highest volume and financial value?
3. How are customer payment methods distributed, and what role do Trade-in alternatives play in transaction values?
4. What does the geographic revenue profile look like across different regional branches in Indonesia?

## 📊 Project Architecture & Tech Stack
* Dataset: 10,000 rows of raw automobile transaction logs containing: `sales_date`, `order_id`, `customer_name`, `branch`, `product_name`, `category`, `price`, `quantity`, `payment_type`, `trade_in`, `discount`, `total_sales`, and `status`.
* Data Engineering: Handled ETL pipelines, missing values imputation, strict order deduplication, text normalization, and exploratory data analysis (EDA) by Python.
* Business Intelligence: Used for data modeling, DAX measurements, and building the final interactive executive dashboard.

## 🧹 Programmatic Data Cleaning Pipeline (Python)
The raw dataset was refined through a Python Pandas pipeline (`Notebook/Showroom_Mobil.ipynb`) executing the following data auditing steps:
1. Missing Value Imputation: Filled blank records in `trade_in` values with `0`.
2. Deduplication: Dropped structural row duplicates based on unique `order_id` validation to safeguard data integrity.
3. Text Standardization: Normalized string spacing and casing inside `payment_type` (e.g., standardizing *Kredit*, *Cash*, *Cash + Trade In*).
4. Temporal Calibration: Converted mixed date values in `sales_date` into standardized `datetime64[ns]` objects for accurate time-series trends.

## 💡 Key Performance Insights
* Overall Sales: Total gross revenue reached Rp 26.02 Billion from 98 finalized transactions (moving a total of 119 physical units). While revenue grew by +12.5% and quantity increased by +10.2% compared to the previous period, our Fulfillment Completion Rate dropped slightly by 2.1% to 89.8%, indicating a need for operational review.
* Monthly Trends: Sales velocity was relatively flat in the first half of 2025, followed by a sharp surge starting in August that spiked into an annual peak in September (approaching Rp 4.0 B), before stabilizing through December.
* Segments & Models: MPVs took the crown as the highest-selling segment generating Rp 9.2 B, closely followed by SUVs at Rp 7.8 B. The top three individual revenue-generating models are the Toyota Avanza 1.5 G CVT (Rp 2.9 B), Honda BR-V 1.5 E CVT (Rp 2.8 B), and Mitsubishi Xpander Ultimate (Rp 2.6 B).
* Regional Profile: Jakarta is our primary growth engine, commanding Rp 6.5 B in total sales, followed by Palembang (Rp 4.8 B) and Karawang (Rp 3.9 B). Meanwhile, the Kendari branch recorded the lowest sales performance at Rp 0.8 B.
* Financing Preferred: Customers heavily favor flexible payment choices. Structured Credit (Kredit) combined with Trade-In options generated 73.5% of our total revenue.


## 🎯 Strategic Business Recommendations
Based on the dashboard insights and data analysis, the following data-driven strategies are recommended for executive stakeholders:

1. Optimize Order Fulfillment Processes: 
   * Insight: Even though total sales value increased by 12.5%, the overall transaction Completion Rate dropped by 2.1% to 89.8%. 
   * Action: Investigate operational bottlenecks causing cancellations or refunds (e.g., in branches like Karawang which shows high refund counts). Streamline the supply chain to minimize fulfillment delays.

2. Capitalize on Peak Seasonal Demand:
   * Insight: Transaction velocity and revenue show an aggressive surge in Q3, peaking heavily in September (approaching Rp 4.0 B).
   * Action: Allocate maximum marketing budget and run aggressive promotional campaigns leading up to August and September. Ensure popular inventory (MPVs and SUVs) is heavily stocked before this high-velocity period to avoid lost sales.

3. Tailor Inventory and Marketing to Segment Preferences:
   * Insight: MPV (Rp 9.2 B) and SUV (Rp 7.8 B) segments dominate corporate revenue, with Toyota Avanza and Honda BR-V as top-selling models. Conversely, City Cars (EV) generate lower revenue share.
   * Action: Maintain high inventory turnover for high-yield MPVs and SUVs. For the EV/City Car segment, re-evaluate the target market or launch educational marketing campaigns focused on eco-friendly efficiency to boost its lower transaction counts.

4. Replicate Jakarta's Success & Intervene in Low-Performing Regions:
   * Insight: Jakarta is the primary revenue powerhouse (Rp 6.5 B), while secondary regions like Palembang and Karawang perform well, but Kendari trails significantly at the bottom (Rp 0.8 B).
   * Action: Document and duplicate Jakarta’s dealership operations, sales training, and local marketing strategies to secondary branches. Conduct a localized market assessment in Kendari to identify if the low revenue is caused by poor brand awareness, pricing misalignment, or mismatch in inventory selection.

5. Enhance Credit Financing Incentives:
   * Insight: Traditional Credit (Kredit) is the most preferred channel commanding 40.8% of total transaction velocity, followed by Cash at 32.7%.
   * Action: Strengthen partnerships with multi-finance companies or banking institutions to offer more competitive credit interest rates or lower down-payment (DP) programs, as this is the primary purchasing driver for customers.

## 📈 Executive Dashboard Interface
Below is the interactive control interface designed for stakeholders:

![Automotif Sales Dashboard](./Dashboard/dashboard.png)

---
📫 **Connect with Me:**
* **LinkedIn:** www.linkedin.com/in/nabila-r-180597244/
* **Email:** bella.rahmahusna@gmail.com
