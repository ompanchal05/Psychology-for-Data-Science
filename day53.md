# 🌐 Day 53 — APIs & Data Collection Basics

## 🎯 Goal
Understand how data is collected from APIs for data science projects.

---

## 📌 What is an API?

API = Application Programming Interface

It allows applications to:
- send data
- receive data
- communicate with other systems

---

## 📊 Why APIs Matter

Data scientists use APIs to collect:
- weather data
- stock data
- social media data
- user activity data

---

## 💻 Basic Python Example

```python
import requests

url = "https://api.example.com/data"
response = requests.get(url)

print(response.json())
