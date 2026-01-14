# Case Study: Customer Health & Troubleshooting (1.2M Records)

## 📌 Step 1: The Problem (Scope & Objectives)
* **Context:** A SaaS platform with **1.2 million login events** showed steady sign-ups, but the "Daily Habit" (retention) of users was fluctuating.
* **The Task:** Build a diagnostic tool to determine if users were leaving due to behavioral shifts or **technical bottlenecks**.
* **The Goal:** Connect technical performance (Error Rates) to user engagement (Stickiness) and identify the specific segments facing friction.

---

## 🛠 Step 2: Data Architecture (The Scaling Phase)
To handle the high volume of logs without lag, I focused on a clean data model.
* **Action:** Generated a **1.2M row synthetic dataset** using Python to simulate real-world system logs.
* **The Model:** Implemented a **Star Schema** in Power BI to allow fast filtering across Regions, Devices, and Subscription types.
* **Metric Logic:** Built a "Golden Triangle" of KPIs: Reach (MAU), Habit (DAU), and Quality (Error Rate).

---

## 🐍 Step 3: Diagnostic Logic (The DAX Methodology)
I developed custom measures to calculate "User Health" and isolate errors across 1.2 million rows.
* **Stickiness Check:** Used the ratio of Daily to Monthly users to measure habit formation, resulting in a **19.69% score**.
* **The Heatmap:** Built an **Error Troubleshooting Matrix** to cross-reference every device and subscription tier.
* **Impact Tracking:** Created a measure to count **Impacted Users** to quantify the human cost of technical errors.

---

## 🎯 Step 4: The Outcome (Business Impact)
* **Root Cause Analysis:** Discovered a global **12.06% Error Rate**, which acts as a ceiling preventing higher user stickiness.
* **Finding:** Pinpointed **North America** as the primary hotspot, representing **39.89% (6K)** of all impacted users.
* **Segment Isolation:** Identified that **Enterprise users on Tablets** were facing the highest error share at **11.57%**.
* **The Result:** Delivered a real-time troubleshooting template that reduced "Time-to-Discovery" from manual log review to interactive filtering dashboard.
