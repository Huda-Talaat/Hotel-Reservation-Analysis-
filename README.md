# 🏨 Hotel Reservations Dashboard

An end-to-end Excel data analysis project analyzing 36,238 hotel bookings from July 2017 to December 2018.


## 📁 Dataset
- **Source:** Hotel Reservations Dataset
- **Records:** 36,238 bookings (after data cleaning)
- **Period:** July 2017 – December 2018


## 🛠️ Tools & Technologies
- **Power Query** — Data cleaning & transformation
- **Power Pivot** — Data modeling (Star Schema)
- **DAX** — Calculated measures
- **Pivot Tables & Charts** — Analysis & visualization
- **Excel Dashboard** — Interactive multi-page reporting


## 🔄 Project Workflow

### 1. Data Cleaning — Power Query
- Removed 37 rows with invalid dates
- Created calculated columns:
  - `total_nights` = weekday nights + weekend nights
  - `Guest_Type` — New vs Repeated
  - `Parking_Request` — With Parking vs No Parking
  - `Day_Type` — Weekday vs Weekend

### 2. Data Modeling — Star Schema
![Star Schema](star_schema.jpeg.jpeg)
Built a Star Schema in Power Pivot:

| Table | Type |
|---|---|
| Fact_Bookings | Fact Table |
| Dim_Date | Dimension |
| Dim_RoomType | Dimension |
| Dim_MealPlan | Dimension |
| Dim_MarketSegment | Dimension |
| Dim_BookingStatus | Dimension |

### 3. DAX Measures
| Measure | Logic |
|---|---|
| Revenue | Total revenue (all bookings) |
| Actual Revenue | Revenue from Not_Canceled bookings only |
| Lost Revenue | Revenue from Canceled bookings only |
| ADR | Actual Revenue ÷ total nights (Not_Canceled) |

### 4. Dashboard — 7 Pages
| Page | Content |
|---|---|
| Home | Navigation landing page |
| Overview | KPIs — Total Bookings, Revenue, Cancellation Rate |
| Cancellation Analysis | Lead time, market segment, room type, time trends |
| Pricing | ADR, room price by channel, room type, month |
| Seasonality | Monthly & quarterly trends, weekday vs weekend |
| Customers | Guest behavior — repeated guests, meal plan, special requests |
| Segments | Market segment comparison — bookings, ADR, revenue |
| Insights & Recommendations | Key findings and actionable recommendations |


## 📊 Key Findings

- **32.8% cancellation rate** — $4.3M in lost revenue out of $11.3M total potential revenue
- **Lead time is the #1 cancellation driver** — bookings made 180+ days ahead cancel at 74% vs 14% for last-minute
- **Engaged guests cancel less** — guests with 3+ special requests cancel at 0%
- **Repeated guests are 20x more loyal** — 1.7% cancel rate vs 33.6% for new guests
- **97.4% of guests never return** — a critical untapped retention opportunity
- **Online segment** drives 64% of bookings and highest ADR ($112) but also highest cancellation at 36.5%
- **Corporate segment** has the lowest cancellation rate (10.9%) but represents only 5.6% of bookings
- **Room Type 6** is the most expensive ($182) yet has the highest cancellation rate (42%)
- **Meal Plan 2** has the highest cancellation rate at 45.6%
- **Q3 is peak season** — highest demand and highest cancellation simultaneously


## 💡 Recommendations

1. **Stricter cancellation policy for long lead times** — require non-refundable deposits for bookings 180+ days ahead
2. **Grow the Corporate segment** — low cancellation, solid ADR, high potential
3. **Investigate why guests don't return** before building any loyalty program
4. **Encourage early engagement** — prompt guests to add parking, meal plans & special requests at booking
5. **Review Room Type 6 & Meal Plan 2** — high cancellation on premium products signals expectation mismatch
6. **Protect Online revenue** — introduce non-refundable booking options for online channel
7. **Seasonal strategy for Q3** — dynamic pricing and stricter policies during peak season




3. DAX Measures

Revenue — total revenue across all bookings

Actual Revenue — revenue from completed (Not_Canceled) bookings

Lost Revenue — revenue lost from canceled bookings

ADR — Actual Revenue divided by total nights for Not_Canceled bookings


4. Dashboard

8 pages: Home, Overview, Cancellation Analysis, Pricing, Seasonality, Customers, Segments, Insights & Recommendations.



📊 Key Findings
32.8% cancellation rate — $4.3M in lost revenue out of $11.3M total

Lead time is the #1 cancellation driver — 180+ days bookings cancel at 74% vs 14% for last-minute

Guests with 3+ special requests cancel at 0%

Repeated guests cancel at 1.7% vs 33.6% for new guests

97.4% of guests never return — a critical retention opportunity

Online segment drives 64% of bookings and highest ADR ($112) but highest cancellation at 36.5%

Corporate segment has the lowest cancellation (10.9%) but only 5.6% of bookings

Room Type 6 is the most expensive ($182) yet has the highest cancellation rate (42%)

Meal Plan 2 has the highest cancellation rate at 45.6%

Q3 is peak season — highest demand and highest cancellation simultaneously


💡Recommendations

1. Stricter cancellation policy for bookings made 180+ days ahead


2. Grow the Corporate segment — low cancellation, solid ADR


3. Investigate why 97.4% of guests never return before building a loyalty program


4. Encourage guests to add parking, meal plans & special requests at booking


5. Review Room Type 6 & Meal Plan 2 — high cancellation on premium products


6. Introduce non-refundable options for Online channel bookings


7. Dynamic pricing and stricter policies during Q3 peak season.
