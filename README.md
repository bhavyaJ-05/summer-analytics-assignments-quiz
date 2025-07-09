# 🚗 Dynamic Pricing for Parking Lots

A real-time dynamic pricing engine that leverages streaming data to **calculate and update parking lot prices** based on **temporal demand patterns**.  
Built using scalable data processing frameworks to **simulate and analyze demand variations** throughout the day.

---

## 📌 Project Overview

This project demonstrates how to implement **dynamic pricing** using a **data stream**.  
By simulating a live environment, the pricing engine computes a **dynamic price** for each parking lot based on **changing demand** over time.

Key components include:

- ⏱️ **Event-time processing**
- 📆 **Daily tumbling window aggregation**
- 📊 **Live output streaming with real-time insights**

---

## 🛠️ Tech Stack

| Tool            | Role                              |
|------------------|------------------------------------|
| **Python**        | Core language for implementation   |
| **Pathway**       | Real-time stream processing engine |
| **Bokeh**         | Interactive data visualization     |
| **Google Colab**  | Development & experimentation      |

---

## 🧭 Architecture Diagram

<p align="center">
  <img src="https://github.com/user-attachments/assets/f8cd7cfa-a996-4d4c-aff0-e47c344a19d8" alt="Architecture Diagram" width="450"/>
</p>


---

## 🔄 Workflow & Architecture Explanation

### 🗂️ 1. Input Source
- A **CSV file** contains historical demand data.
- It is **replayed as a live data stream** using `Pathway` to simulate real-time input.

---

### 🧮 2. Streaming & Aggregation
- The data is **windowed using a daily tumbling window** based on `event-time`.
- Grouping is done by `(lot_id, day)` or similar logical keys.
- This enables **temporal aggregation** of demand statistics.

---

### 💸 3. Dynamic Pricing Logic
- A **pricing function** is applied based on aggregated demand:
  - Surge pricing
  - Inventory-based adjustments
  - Time-of-day or day-of-week modifiers

---

### 🤖 4. Optional: ML Integration
- A **machine learning model** (e.g., regression) can be plugged in.
- It is trained offline and used for **inference during streaming**.

---

### 📤 5. Output
- Final computed prices are **exposed as a live table**.
- This can be connected to:
  - Dashboards
  - Real-time APIs
  - Storage or logging layers

---

