# Problem Statment :
Logistics and supply chain company which is the largest and fastest-growing fully integrated player in India by revenue in Fiscal 2021.They aim to build the operating system for commerce, through a combination of world-class infrastructure, logistics operations of the highest quality, and cutting-edge engineering and technology capabilities.

The Data team builds intelligence and capabilities using this data that helps them to widen the gap between the quality, efficiency, and profitability of their business versus their competitors.

Objective :     
The company wants to understand and process the data coming out of data engineering pipelines:

• Clean, sanitize and manipulate data to get useful features out of raw fields

• Make sense out of the raw data and help the data science team to build forecasting models on it


Sure! Here's a **simplified version** of your content, written in clear and straightforward language — ideal for documentation, presentations, or code comments in a Colab notebook:

---

## 🧹 **Step-by-Step Data Cleaning & Feature Preparation**

### 🔧 **Basic Data Cleaning and Exploration**

* Fill in or remove any **missing values**.
* Understand how the data is structured (columns, types, etc.).
* **Merge rows** using `trip_uuid`, `source_center`, and `destination_center` to get a cleaner dataset.
* Create useful columns (**features**) from existing ones:

  * **Destination Name**: Split it to extract city, place code, and state.
  * **Source Name**: Do the same here — extract city, place code, and state.
  * **Trip Creation Time**: Break it into **day**, **month**, and **year**.

---

### 🧠 **In-Depth Analysis and Feature Engineering**
* Removed unusable features like segment_time due to missing/irrelevant data.

  Merged rows by **trip_uuid** and grouped by **source_center**, **destination_center**.

* Do **hypothesis testing** between:

  1. **Aggregated `actual_time`** vs **aggregated OSRM time**
  2. **Aggregated `actual_time`** vs **aggregated segment actual time**
  3. **Aggregated actual_distance_to_destination** vs **aggregated segment osrm_distance**

---

### 📉 **Handling Outliers and Scaling**

* Look for **outliers** in numeric columns using **plots** (like boxplots).
* Remove or handle outliers using the **IQR method**.
---

Let me know if you'd like a **code version** of each of these steps!

