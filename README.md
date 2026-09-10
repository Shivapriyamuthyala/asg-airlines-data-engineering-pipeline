# ✈️ ASG Airlines - End-to-End Data Engineering Pipeline

> Campus Placement Project | Data Quality + ETL + Gold Layer

**Problem:** ASG Airlines data had 72 UNKNOWN airlines, 100 INVALID payments, overnight flight time bug (negative durations), PII leaks.

**My Solution:**
- **Bronze:** Ingested 4 Excel sheets (flights, bookings, payments, passengers) = 1000+ rows
- **Silver:** Cleaned using Python/Pandas
    - Airline fix: Used flight_id prefix (6F -> IndiGo, SJ -> SpiceJet)
    - Overnight fix: If duration < 0 then +1440 mins (123 flights fixed)
    - Payment fix: Median imputation by payment_method
- **Gold:** Built Star Schema (fact_bookings) for Power BI
- **Data Quality:** 15 checks (nulls, duplicates, anomalies)

**Tech Stack:** Python, Pandas, SQL, Data Quality, Excel

**Key Insights:**
- Busiest Route: BOM-CCU (90 flights)
- 12.2% flights are overnight
- Median Ticket: ₹9,044

**How to Run:**
pip install -r requirements.txt
python src/etl_pipeline.py

**Author:** Shiva Priya Muthyala | Seeking Data Engineer Intern
