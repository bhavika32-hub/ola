# Ola Ride Cancellation Analysis

---

## Problem Statement

The objective was to analyze ride data to identify key reasons behind ride cancellations, incomplete rides, and associated revenue loss, and suggest data-driven strategies to improve booking success rate, operational efficiency, and customer experience.

---

## Business Objective

To identify key factors affecting ride cancellations and improve overall platform efficiency by:

* Reducing cancellation rate and minimizing revenue loss
* Improving ride success rate  
* Enhancing customer and driver experience  
* Optimizing operational decision-making using data  

---

## Tools & Technologies

* Excel – Data Cleaning and Preparation  
* SQL – Exploratory Analysis and Business Queries  
* Power BI – Dashboard creation, Data visualization  

---

## Dataset

* 50K+ ride records  
* Data included: booking status, cancellation reasons, driver behavior, ride details, and revenue impact  

---

## KPI Tracking

* Business KPIs: Bookings, Revenue, Success Rate, Total Revenue Loss 
* Customer KPIs: Customer cancellation %, ratings  
* Driver KPIs: Driver cancellation %, driver rating  
* Operational KPI: Cancellation rate by vehicle type  

---

## Key Insights

* 30% cancellations occurred because drivers did not move toward pickup location, leading to customer frustration  
* 25% cancellations were due to drivers asking customers to cancel  
* 15% were caused by driver personal or vehicle-related issues  
* 14% cancellations were due to AC or comfort-related complaints  
* Highest bookings and cancellations observed on Monday, Tuesday, and Wednesday
* Total revenue loss of ₹21M was observed due to cancellations and driver-related issues  
* ₹16M loss was due to ride cancellations, indicating high demand leakage  
* ₹5M loss was due to driver not found cases, showing supply-side inefficiency  
* Around 40% of incomplete rides were due to vehicle breakdown issues, indicating operational and maintenance gaps  

**Overall Insight:** Driver behavior, vehicle condition, and peak-day operational pressure are the major contributors to cancellations and revenue loss.

---

## SQL Analysis

SQL was used to extract insights, calculate KPIs, and understand booking, cancellation, and customer behavior patterns.

### Key Areas Covered

**1. Booking & Revenue Analysis**
* Total bookings by vehicle type  
* Revenue contribution by vehicle type  
* Successful vs cancelled bookings  

**2. Customer Analysis**
* Total rides per customer  
* Frequent customers (5+ rides)  
* Top customers by number of bookings  

**3. Cancellation Analysis (Core Focus)**
* Customer vs Driver cancellations  
* Cancellation reasons (frequency-based)  
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

## Business Recommendations (with Reason)

### 1. Driver Accountability & Incentives
* Penalize or warn drivers who do not move toward pickup location  
* Provide incentives for drivers with high acceptance and low cancellation rates  
**Reason:** Improves ride completion and driver responsibility  

---

### 2. Driver Quality Monitoring
* Identify drivers with repeated cancellations  
* Provide training or restrict access for poor performers  
**Reason:** Ensures platform reliability and service quality  

---

### 3. Vehicle & Comfort Compliance
* Regular vehicle inspections (AC, cleanliness, condition)  
* Remove non-compliant drivers  
**Reason:** Improves customer satisfaction and trust  

---

### 4. Demand-Based Optimization
* Focus driver availability on high-demand days (Mon–Wed)  
* Optimize driver allocation during peak booking periods  
**Reason:** Reduces cancellations during high-demand pressure  

---

### 5. Vehicle Maintenance & Breakdown Reduction
* Regular vehicle health checks and preventive maintenance  
* Monitor vehicles with repeated breakdown history  
* Partner with service centers for quick repair turnaround  
**Reason:** Around 40% incomplete rides were due to vehicle breakdowns, impacting ride completion and customer trust  

---

## Success Measurement (Expected Impact)

* Reduction in overall cancellation rate  
* Improvement in ride success rate and customer satisfaction  
* Decrease in driver-related complaints and repeated cancellations  
* Reduction in revenue loss (~₹21M impact area)
* Better operational efficiency through improved driver allocation  
