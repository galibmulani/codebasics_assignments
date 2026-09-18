# 🏨 Codebasics Resume Project Challenge — Hospitality Analytics

**Resume Project Challenge conducted by Codebasics**

This project was completed as part of the **Hospitality Challenge**, where the objective was to analyze hospitality booking data and create business reports using **Excel Pivot Tables, Power Pivot, Data Modeling, and DAX measures**.

---

## 📌 Project Overview

The goal of this project was to build interactive analytical reports from hospitality booking data and extract meaningful business insights related to:

* Property performance
* Booking volume
* Revenue generation
* Guest ratings
* Booking platform performance
* Weekly trends

The project uses two CSV datasets:

* `fact_bookings`
* `dim_properties`

The data was connected through a **Data Model** and analyzed using **Power Pivot, Pivot Tables, and DAX measures**.

---

## 🎯 Business Objective

The analysis focuses on answering questions such as:

* Which properties generate the highest revenue?
* How does booking performance change from month to month?
* Which properties have strong booking growth?
* Are high-revenue properties also receiving good guest ratings?
* Which booking platforms contribute the most bookings and revenue?
* Does an increase in bookings always result in proportional revenue growth?

These insights can help stakeholders identify performance trends and areas that may require further investigation.

---

## 🛠️ Tools & Technologies

* **Microsoft Excel**
* **Excel Tables**
* **Power Query**
* **Power Pivot**
* **Data Model**
* **Pivot Tables**
* **DAX**

---

## 📂 Dataset

The project uses two CSV files:

### `fact_bookings`

Contains booking-level information used for analyzing:

* Bookings
* Revenue
* Ratings
* Booking platforms
* Week/month performance

### `dim_properties`

Contains property-related information used to analyze performance by:

* Property
* City
* Category

---

# 🔄 Project Workflow

The overall workflow followed in this project was:

**Raw CSV Data → Power Query → Data Model → Relationship → Power Pivot → DAX Measures → Pivot Tables → Business Insights**

---

## 1️⃣ Connect Data Using Excel & Power Query

Created a new Excel workbook and imported both CSV files using:

**Data → From Text/CSV**

The datasets were then opened in **Power Query Editor**.

The tables were loaded into the **Data Model** using the **Create Only Connection** option.

---

## 2️⃣ Establish Relationship Between Fact & Dimension Tables

Opened **Power Pivot** from Excel and switched to **Diagram View**.

Created a relationship between:

`dim_properties[property_id]`

and

`fact_bookings[property_id]`

This creates a **1-to-many (1:M)** relationship where the property dimension can filter the booking fact table.

### Data Model Structure

```text
dim_properties
       │
       │ property_id
       │
       ▼
fact_bookings
```

This relationship allows property-level information to be used while analyzing booking-level data.

---

# 📊 Reports Created

## 3️⃣ All Properties Performance Report

This report provides a monthly performance overview of the properties.

### Pivot Table Configuration

**Rows**

* `month`
* `property_name`

**Values**

* Total Bookings
* Total Revenue Generated
* Average Rating

**Filters**

* `category`
* `city`

### DAX Functions Used

```text
COUNT()     → Total Bookings
SUM()       → Total Revenue Generated
AVERAGE()   → Average Rating
```

### Purpose

The report helps compare properties across different months using three key metrics:

* Booking activity
* Revenue generation
* Guest ratings

---

## 4️⃣ Booking Platform by Week Report

This report analyzes booking performance across different booking platforms and weeks.

### Pivot Table Configuration

**Rows**

* `week_no`
* `booking_platform`

**Values**

* Total Bookings
* Total Revenue Generated

**Filters**

* `property_name`
* `category`

### Purpose

The report helps understand:

* Weekly booking trends
* Revenue contribution by platform
* Changes in booking activity over time
* Differences between booking volume and revenue

---

# 📈 Key Insights

## 🏨 All Properties Performance Report

### 1. Atliq Exotica — Strong Revenue Performance

**Atliq Exotica** was the top revenue generator in both analyzed months and also maintained strong ratings.

This indicates consistent revenue performance across the reported period.

### 2. Atliq Blu — Strong Booking Growth

Atliq Blu showed a significant increase in bookings:

**June:** 85 bookings
**July:** 132 bookings

Its average rating also increased:

**4.40 → 4.58**

This shows strong growth in booking activity along with an improvement in the reported rating.

### 3. Atliq City — Revenue vs Rating Difference

Atliq City generated relatively high revenue, particularly in July, while its average rating remained around **3.0**.

This creates an area worth investigating further: why is revenue relatively strong while guest ratings remain comparatively low?

### 4. Atliq Seasons — Lowest Reported Rating

Atliq Seasons recorded the lowest average rating:

**2.30 → 2.50**

Despite generating moderate revenue, the relatively low rating suggests that guest feedback and operational factors may require further investigation.

> **Note:** The analysis identifies these patterns from the available booking, revenue, and rating data. Additional operational data would be required to determine the underlying causes.

---

# 📅 Booking Platform by Week — Key Insights

### 1. W28 — Highest Overall Performance

W28 recorded:

* **82 bookings**
* **₹7.31 lakh revenue**

It contributed approximately:

* **38% of total bookings**
* **35% of total revenue**

among the four analyzed weeks.

---

### 2. W24 — Lowest Weekly Performance

W24 recorded:

* **32 bookings**
* **₹3.33 lakh revenue**

Compared with W23:

* Bookings decreased by approximately **40%**
* Revenue decreased by approximately **36%**

---

### 3. Strong Recovery in W27 and W28

| Week | Bookings |    Revenue |
| ---- | -------: | ---------: |
| W27  |       50 | ₹4.98 lakh |
| W28  |       82 | ₹7.31 lakh |

From W27 → W28:

* Bookings increased by approximately **64%**
* Revenue increased by approximately **47%**

This also shows that revenue did not increase at the same rate as booking volume.

---

### 4. "Others" — Largest Contributor

Across the four weeks, **Others** recorded:

* **89 bookings**
* **₹8.92 lakh revenue**

This represents approximately:

* **41% of total bookings**
* **43% of total revenue**

---

### 5. Journey — Significant Booking Channel

The report contains two separate rows labelled **Journey**.

If these rows represent the same booking platform, combining them gives:

* **57 bookings**
* **₹5.12 lakh revenue**

This would make Journey one of the largest contributors by both bookings and revenue.

> ⚠️ **Data Quality Note:** The two Journey rows should be verified before treating them as a single category. They have been kept separate in the original report rather than being automatically combined.

---

### 6. Direct Offline — Lower Booking Volume

Direct Offline recorded:

* **11 bookings**
* **₹1.08 lakh revenue**

Although its booking volume was relatively low, its revenue per booking was comparatively high.

This could be investigated further by comparing it with other channels and, if available, channel acquisition or commission costs.

---

### 7. Booking Growth vs Revenue Growth

From W27 → W28:

**Bookings:** +64%
**Revenue:** +47%

Therefore, the increase in revenue was lower than the increase in booking volume.

This indicates that the **average revenue per booking decreased in W28**, even though W28 generated the highest total revenue.

---

# 💡 Key Learnings

## 🔹 Excel & Pivot Tables

Through this project, I learned how to:

* Import and work with multiple CSV files in Excel.
* Create Pivot Tables using the Excel Data Model.
* Organize fields into **Rows, Values, and Filters**.
* Summarize large datasets using business KPIs.
* Analyze bookings, revenue, and average ratings.
* Format Pivot Table values for better readability.

---

## 🔹 Power Query & Data Modeling

I gained practical experience in:

* Connecting CSV files using **Data → From Text/CSV**.
* Opening datasets in **Power Query Editor**.
* Loading tables into the **Data Model**.
* Creating relationships between fact and dimension tables.
* Understanding the purpose of **Fact and Dimension tables** in analytical models.

The main relationship used was:

```text
dim_properties[property_id]
              ↓
fact_bookings[property_id]
```

---

## 🔹 Power Pivot

I learned how to:

* Manage tables inside the Data Model.
* Create relationships using **Diagram View**.
* Build Pivot Tables directly from the Data Model.
* Analyze data across multiple related tables.

---

## 🔹 DAX

I practiced creating measures using basic DAX functions:

| Function    | Purpose                                                |
| ----------- | ------------------------------------------------------ |
| `COUNT()`   | Calculate total bookings                               |
| `SUM()`     | Calculate total revenue                                |
| `AVERAGE()` | Calculate average rating                               |
| `MAX()`     | Identify the highest value within the required context |

I also learned that writing DAX is not only about knowing individual functions.

Understanding **filter context, relationships, and the business requirement** is equally important when creating meaningful measures.

---

## 🔹 Business Analysis

This project helped me improve my ability to:

* Identify trends across different weeks and months.
* Compare booking volume with revenue.
* Analyze booking platform contributions.
* Identify differences between booking growth and revenue growth.
* Convert numerical findings into business questions.
* Identify areas that require further investigation.

---

# 📷 Report Preview

### All Properties Performance Report

![all_properties_performance](./screenshot/all_properties_performance_screenshot.png)

### Booking Platform by Week

![booking plateform by week](./screenshot/booking_plateform_by_weeks.png)


---

# 🎯 Skills Demonstrated

**Excel | Pivot Tables | Power Query | Power Pivot | Data Modeling | DAX | Data Analysis | Business Insights**

---

# 🚀 Overall Learning

This project helped me understand the complete analytics workflow:

> **Raw Data → Power Query → Data Model → Power Pivot → DAX Measures → Pivot Tables → Business Insights**

More importantly, I learned that a Data Analyst's role is not only to create reports.

The goal is to:

**Understand the business problem → Analyze the data → Identify meaningful patterns → Communicate insights → Ask better business questions**

---

## 🙏 Acknowledgement

This project was completed as part of the **Codebasics Resume Project Challenge — Hospitality Challenge**.

Special thanks to **Codebasics** for providing the project framework and datasets that helped me gain practical experience in Excel, Power Query, Power Pivot, Data Modeling, and DAX.

