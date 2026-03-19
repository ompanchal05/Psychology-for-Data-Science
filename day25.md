# 🧠 Day 25 — Feature Engineering (Behavioral Data Science)

## 🎯 Goal of Day 25

Today you will:

✔ Convert raw data → meaningful features  
✔ Add psychological meaning to variables  
✔ Prepare data for machine learning  

This is the step where:
> Normal data scientists stop at numbers  
> You go deeper into **human behavior**

---

# 🧠 What is Feature Engineering?

Feature engineering means:

> Transforming raw data into useful inputs for models.

Example:

Raw → tenure = 12 months  
Feature → "Low Habit Strength"

---

# 🧩 Step 1 — Identify Raw Features

Example dataset columns:

- tenure  
- monthly_charges  
- total_charges  
- support_calls  
- contract_type  
- churn  

---

# 🔍 Step 2 — Convert Data into Behavioral Features

Now apply psychology.

---

## 🔹 1. Habit Strength

```python
if tenure < 6 → Low Habit
if tenure 6–24 → Medium Habit
if tenure > 24 → Strong Habit
