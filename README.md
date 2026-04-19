## 🚖 Ola Ride Cancellation Analysis

### 📌 Problem Statement

The objective was to analyze ride data to identify key reasons behind ride cancellations and suggest data-driven strategies to improve booking success rate and customer experience.

---

### 🛠️ Tools Used

* SQL
* Power BI

---

### 📊 Dataset

* 50K+ ride records
* Data included: booking status, cancellation reasons, driver behavior, and ride details

---

### 🔍 Key Analysis Performed

* Analyzed **cancellation patterns across different scenarios**
* Identified **driver-side vs customer-side cancellation reasons**
* Evaluated **impact of driver behavior on ride success rate**
* Studied **operational and service-related issues affecting ride completion**

---

### 🧾 SQL Analysis

SQL was used to extract insights, calculate KPIs, and understand booking, cancellation, and customer behavior patterns.

#### 🔹 Key Areas Covered

**1. Booking & Revenue Analysis**

* Total bookings by vehicle type
* Revenue contribution by vehicle type
* Successful vs cancelled bookings

**2. Customer Analysis**

* Total rides per customer
* Frequent customers (more than 5 rides)
* Top customers by number of bookings

**3. Cancellation Analysis (Core Focus)**

* Customer vs Driver cancellations
* Cancellation reasons (sorted by frequency)
* Vehicle-type-wise cancellation trends
* Location-wise cancellation hotspots

**4. Ratings & Experience Analysis**

* Average driver and customer ratings
* Low-rating + high-cancellation locations

**5. Operational Insights**

* High-demand pickup locations
* Payment method usage (e.g., UPI)
* Incomplete rides and reasons

---

### 🔍 Sample SQL Queries

```sql
-- Total bookings per vehicle type
SELECT vehicle_type, COUNT(*) AS total_bookings
FROM bookings
GROUP BY vehicle_type;

-- Customer vs Driver cancellations
SELECT 'Customer Cancel' AS type, COUNT(*) AS total
FROM bookings
WHERE cancelled_rides_by_customer = 1
UNION ALL
SELECT 'Driver Cancel' AS type, COUNT(*) AS total
FROM bookings
WHERE cancelled_rides_by_driver = 1;

-- Location-wise cancellations
SELECT pickup_location,
       COUNT(*) AS total_rides,
       SUM(cancelled_rides_by_customer + cancelled_rides_by_driver) AS cancellations
FROM bookings
GROUP BY pickup_location
ORDER BY cancellations DESC;
```

---

### 💡 Key Insights

Analysis revealed that ride cancellations were primarily driven by driver-related issues:

* ~30% cancellations occurred because **drivers did not move toward pickup location**, leading to customer frustration
* ~25% cancellations were due to **drivers asking customers to cancel**
* ~15% were caused by **driver personal or vehicle-related issues**
* ~14% cancellations were due to **AC or comfort-related complaints**

👉 Overall insight:
Driver behavior and availability were the **major drivers of cancellations**, with delayed pickup movement being a key customer pain point

---

### 🚀 Business Recommendations (with Reason)

#### 1. Driver Accountability & Incentives

* Penalize or warn drivers who do not move toward pickup location
* Provide incentives for drivers with **high acceptance and low cancellation rates**
  → Reason: Encourages responsible driver behavior and improves ride completion

#### 2. Driver Quality Monitoring

* Identify drivers with repeated cancellations
* Provide training or temporarily restrict access for poor performers
* Improve onboarding standards
  → Reason: Ensures only reliable drivers remain active on the platform

#### 3. Vehicle & Comfort Compliance

* Conduct regular vehicle inspections (AC, cleanliness, condition)
* Penalize or remove non-compliant drivers
  → Reason: Improves customer experience and reduces comfort-related cancellations

---

### 📊 Success Measurement (Expected Impact)

* Potential reduction in overall cancellation rate**
* Improvement in ride success rate and customer satisfaction**
* Decrease in driver-related complaints and repeated cancellations**

---

### 📌 Business Impact (Potential)

* Identified key operational gaps affecting **ride completion and customer experience**
* Insights can support **better driver management and monitoring strategies**
* Recommendations may help improve **platform reliability and user trust**

---


