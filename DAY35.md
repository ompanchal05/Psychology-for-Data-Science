# 🚀 Day 35 — Advanced Recommendation System (Hybrid)

## 🎯 Goal
Improve recommendation system using hybrid approach:
- Collaborative filtering
- Content-based filtering

---

## 📊 Key Concepts

- Collaborative → similar users  
- Content-based → similar items  
- Hybrid → combine both  

---

## ⚙️ Steps

1. Use user-item interaction data  
2. Add item features (category, type, etc.)  
3. Compute:
   - user similarity  
   - item similarity  
4. Combine both scores  
5. Generate better recommendations  

---
🧠 Psychology Insight

-Familiarity → similar content
-Novelty → new recommendations
-Balance → best user experience
---

🏁 Outcome

- ✔ Improved recommendation system
- ✔ Better personalization
- ✔ Balanced suggestions
---
## 💻 Code (Basic Idea)

```python
# Hybrid Score
final_score = (user_similarity_score + item_similarity_score) / 2
