# NTI_Final_project
🏨 Hotel Booking Data Analysis
A full end-to-end data analytics project on a hotel booking dataset of ~600,000 records, covering data cleaning, preprocessing, feature engineering, customer segmentation (RFM), data modeling, and an interactive Power BI dashboard.
---
📌 Project Overview
This project analyzes hotel booking behavior to uncover insights around booking trends, cancellations, revenue, guest demographics, and customer value. The pipeline takes raw booking data through cleaning and preprocessing, engineers new features (including RFM-based customer segmentation), models the data, and visualizes the results in an interactive Power BI dashboard.
🎯 Objectives
Explore booking patterns across cities, hotels, room types, and booking channels
Clean and prepare a large-scale (600K row) real-world dataset
Engineer meaningful features (stay length, weekend bookings, domestic vs. international, booking counts, etc.)
Segment guests using RFM (Recency, Frequency, Monetary) analysis into loyalty tiers (Bronze, Silver, Gold, Premium, Titanium)
Build a relational data model and an interactive dashboard for business insights
🛠 Tools & Technologies
Python (Pandas, NumPy, Matplotlib) — EDA, cleaning, preprocessing, feature engineering, RFM segmentation
Power BI — data modeling and dashboard/visualization
Jupyter Notebook — analysis workflow
📊 Dataset
Size: ~600,000 rows
Key columns: `booking_id`, `hotel_id`, `hotel_name`, `city`, `country`, `hotel_stars`, `room_type`, `guest_name`, `guest_email`, `adults`, `children`, `checkin_date`, `checkout_date`, `nights`, `booking_date`, `booking_channel`, `payment_method`, `price_per_night_usd`, `total_price_usd`, `booking_status`, `guest_rating`, `special_requests`
🔄 Project Workflow
1. Dataset & EDA
Initial exploration of shape, data types, summary statistics, missing values, and duplicates. Early insights on average price by hotel stars, booking status distribution, average nights/price per booking, and most common room type/booking channel.
2. Data Cleaning
Removed duplicate rows
Handled missing values (`guest_rating` filled with mean, `special_requests` filled with `"No Request"`)
Converted date columns to proper datetime format
Treated outliers in `price_per_night_usd` and `total_price_usd` using the IQR method
3. Data Preprocessing
Validated data consistency (e.g., recalculated nights vs. recorded nights, price ratio checks)
Checked for invalid records (zero/negative prices, zero guests)
Standardized `booking_status` into a simplified `is_cancelled` flag (Cancelled/No-Show → "Cancelled", others → "Confirmed")
4. Feature Engineering
Date-based features: `checkin_year`, `checkin_month`, `checkin_weekday`, `checkin_is_weekend`
`length_of_stay_days` from check-in/check-out dates
`is_domestic_booking` flag (Egypt vs. other countries)
Aggregated features: `hotel_booking_count`, `city_booking_count`
RFM Segmentation:
Recency, Frequency, and Monetary value calculated per guest
Scored 1–5 on each dimension via quantile ranking
Combined into an RFM score and mapped to customer tiers: Bronze, Silver, Gold, Premium, Titanium
5. Data Modeling & Summarization
Structured and modeled the cleaned/engineered dataset in Power BI (relationships, measures, and summarized tables) to support the dashboard layer.
6. Visualization & Dashboard
Interactive Power BI dashboard presenting booking trends, revenue, cancellations, guest segments, and hotel/city performance.

📁 Repository Contents
`Final_project_python_part_.ipynb` — full Python workflow (EDA → cleaning → preprocessing → feature engineering → RFM segmentation)
`Data_modelling.pbix` — Power BI data model
`Final_Pro.pbix` — final Power BI dashboard/report
`hotel_bookings_RFM.csv` — output file with RFM scores and customer segments per guest
🚀 How to Run
Clone the repository:
```bash
   git clone https://github.com/zeinaozoris11/NTI_Final_project.git
   ```
Open `Final_project_python_part_.ipynb` in Jupyter Notebook/Lab and run the cells in order (requires `pandas`, `numpy`, `matplotlib`).
Open `Final_Pro.pbix` in Power BI Desktop to explore the dashboard.
📈 Key Insights
Clear segmentation of guests into loyalty tiers (Bronze → Titanium) based on RFM behavior
Cancellation and no-show patterns tracked via a standardized `is_cancelled` flag
Booking trends by season, weekday/weekend, and domestic vs. international guests
Revenue and pricing patterns across hotel star ratings, cities, and room types
---
👥 Team & Roles
Member	Role
Nourhan Taha	Dataset & EDA
Doaa Gamal	Data Cleaning & PowerPoint
Malak Mohamed	Data Preprocessing
Zeina Mohamed	Feature Engineering
Beshoy Hanna	Data Modeling & Summarization
Sohaib	Visualization & Dashboard
📂 Project Repository: NTI_Final_project
