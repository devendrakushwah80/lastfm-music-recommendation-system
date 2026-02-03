# Music Recommendation System using Collaborative Filtering

## 📌 Overview
This project implements a **music artist recommendation system** using the
**Last.fm HetRec 2011 dataset**.  
The system recommends new artists to users based on **listening behavior of
similar users**, following the principles of **Collaborative Filtering**.

The goal of this project is to understand how real-world recommendation systems
work using user interaction data.

---

## 🎯 Objective
- Analyze user–artist listening behavior
- Handle sparse interaction data
- Build a **User-Based Collaborative Filtering** recommender
- Generate personalized artist recommendations

---

## 📂 Dataset
**HetRec 2011 – Last.fm Dataset**
- 1,892 users
- 17,632 artists
- 92,834 user–artist listening interactions

Files used:
- `user_artists.dat` → user–artist listening counts
- `artists.dat` → artist metadata

---

## 🧠 Recommendation Approach

### ✔ Collaborative Filtering
This system uses **Collaborative Filtering**, which relies on:
- User IDs
- Artist IDs
- Listening counts

No artist metadata (genre, tags, etc.) is used for recommendation.

---

### ✔ User-Based Collaborative Filtering
Steps:
1. Create a **User–Artist interaction matrix**
2. Compute **Cosine Similarity** between users
3. Identify users with similar listening patterns
4. Recommend artists liked by similar users
5. Exclude artists already listened to by the target user

---

## 📊 Exploratory Data Analysis (EDA)

Key insights from EDA:
- Listening behavior is highly **skewed**
- Most users listen to only a few artists
- Few artists are very popular, while most are niche
- The user–artist matrix is **highly sparse**

These characteristics justify the use of **collaborative filtering**.

---

## 🔧 Implementation Details

- User–Artist Matrix using `pivot_table`
- Similarity measure: **Cosine Similarity**
- Weighted aggregation of neighbor preferences
- Removal of already listened artists from recommendations

---

## ✨ Add-ons Implemented
- Artist name mapping for readable output
- Artist-based similarity (optional add-on)
- Explainable recommendations (optional)
- Simple evaluation using Precision@K (basic)

---

## 🚀 Example Usage

```python
recommend_artists(user_id=2, n_recommendations=5)
