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

### 🧠 SQL Analysis Approach

To understand ride performance and cancellation patterns, SQL queries were used to explore the dataset from multiple perspectives:

#### 📊 Booking & Revenue Analysis

* Total bookings by vehicle type
* Revenue contribution by vehicle category
  👉 Purpose: Identify high-demand and high-revenue segments

#### 📈 Customer Behavior Analysis

* Total rides per customer
* Frequent users (more than 5 rides)
  👉 Purpose: Understand customer engagement

#### ❌ Cancellation Analysis (Core Focus)

* Customer vs driver cancellations
* Cancellation reasons distribution
* Vehicle-type and location-wise cancellations
  👉 Purpose: Identify root causes of cancellations

#### ⭐ Service Quality Analysis

* Average driver and customer ratings
* Low-rating & high-cancellation locations
  👉 Purpose: Detect service quality issues

#### 📍 Location-Based Insights

* High booking locations
* Locations with maximum cancellations
  👉 Purpose: Identify geographic problem areas

---

### ⚙️ Example SQL Query

SELECT 'Customer Cancel' AS type, COUNT(*) AS total
FROM bookings
WHERE cancelled_rides_by_customer = 1
UNION ALL
SELECT 'Driver Cancel' AS type, COUNT(*) AS total
FROM bookings
WHERE cancelled_rides_by_driver = 1;

---

### 💡 Key Insights

Analysis revealed that ride cancellations were primarily driven by driver-related issues:

* ~30% cancellations occurred because **drivers did not move toward pickup location**, leading to customer frustration
* ~25% cancellations were due to **drivers asking customers to cancel**
* ~15% were caused by **driver personal or vehicle-related issues**
* ~14% cancellations were due to **AC or comfort-related complaints**

👉 Overall Insight:
Driver behavior and availability were the **major drivers of cancellations**, with delayed pickup movement being a key customer pain point

---

### 🚀 Business Recommendations (with Reason)

#### 1. Driver Accountability & Incentives

* Penalize or warn drivers who do not move toward pickup location
* Provide incentives for drivers with **high acceptance and low cancellation rates**
  → Reason: Encourages responsible behavior and improves ride completion

#### 2. Driver Quality Monitoring

* Identify drivers with repeated cancellations
* Provide training or restrict access for poor performers
* Improve onboarding standards
  → Reason: Ensures platform reliability

#### 3. Vehicle & Comfort Compliance

* Conduct regular vehicle inspections (AC, cleanliness, condition)
* Penalize or remove non-compliant drivers
  → Reason: Improves customer experience

---

### 📊 Success Measurement (Expected Impact)

* Potential reduction in **overall cancellation rate**
* Improvement in **ride success rate and customer satisfaction**
* Decrease in **driver-related complaints and repeated cancellations**

---

### 📌 Business Impact (Potential)

* Identified operational gaps affecting **ride completion and user experience**
* Insights can support **better driver management strategies**
* Recommendations may help improve **platform reliability and customer trust**

---

### 📎 Project Links

* GitHub: https://github.com/bhavika_gandhi
