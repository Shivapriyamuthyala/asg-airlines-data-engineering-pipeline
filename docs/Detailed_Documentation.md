# Detailed Documentation

## 1. Problem Statement
ASG Airlines data was corrupted.

## 2. Data Cleaning
- 72 UNKNOWN airlines fixed using flight_id prefix (6F->IndiGo)
- 123 negative durations fixed for overnight flights (added 1440)
- 100 INVALID payments fixed with median

## 3. Architecture
Bronze (Raw Excel) -> Silver (Cleaned CSV) -> Gold (Fact Table)

## 4. Files
- .ipynb - ETL logic
- .pbix - Power BI dashboard with 4 visuals (Route traffic, Revenue, Booking Status)
- sql/ - 4 analytical queries

## 5. Results
Busiest route BOM-CCU, 12.2% overnight flights.
