# 🤖 Day 34 — Recommendation System (Basic Implementation)

## 🎯 Goal
Build a simple recommendation system using collaborative filtering.

---

## 📊 Dataset
Sample user-item interaction data:

- user_id  
- item  
- rating  

---

## ⚙️ Steps

1. Load dataset  
2. Create user-item matrix  
3. Fill missing values  
4. Compute similarity (cosine similarity)  
5. Recommend items based on similar users  

---

## 💻 Code (Basic)

```python
import pandas as pd
from sklearn.metrics.pairwise import cosine_similarity

# Sample Data
data = {
    "user_id": [1,1,1,2,2,3,3,3],
    "item": ["A","B","C","A","C","B","C","D"],
    "rating": [5,4,3,4,5,2,5,4]
}

df = pd.DataFrame(data)

# User-Item Matrix
matrix = df.pivot_table(index='user_id', columns='item', values='rating').fillna(0)

# Similarity
similarity = cosine_similarity(matrix)

# Recommend Function
def recommend(user_id):
    sim_scores = similarity[user_id-1]
    similar_user = sim_scores.argsort()[-2]
    return matrix.iloc[similar_user].sort_values(ascending=False)

print(recommend(1))
```

## 🧠 Psychology Insight
- Similar users → similar behavior
- Repeated interaction → habit
- High rating → strong preference
---

## 🏁 Outcome
- Basic recommendation system built
- Understand user similarity
- Ready for improvement
---

## 💬 Summary
- Recommendation systems use user behavior + similarity to suggest items.
