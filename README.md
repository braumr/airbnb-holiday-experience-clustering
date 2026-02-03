# 🎄✈️ Holiday Travel Experience Clustering Using Airbnb Reviews

## 📌 Overview
This project explores how holiday travel experiences differ across global cities by analyzing Airbnb review text alongside market characteristics.  
Rather than predicting prices or ratings, the goal is descriptive insight: uncovering whether cities exhibit recurring holiday experience profiles when sentiment, emotional tone, and market features are considered together.

Using unsupervised clustering, cities are grouped independently for major holidays to reveal patterns in traveler experience that go beyond simple positive/negative sentiment.

---

## ❓ Key Questions
- Do cities exhibit consistent experience patterns during major holidays?
- Is sentiment polarity alone sufficient to describe holiday travel experiences?
- How do emotional tone and market dynamics shape these experiences?

---

## 📊 Data
- **Source:** Inside Airbnb  
- **Reviews analyzed:** ~1.6 million  
- **Listings analyzed:** ~477,000  
- **Cities:** 20 global cities (U.S. & international)

---

## 🎉 Holidays Analyzed
- 🎄 Christmas  
- 🎆 New Year’s  
- ❤️ Valentine’s Day  
- 🎃 Halloween  
- 🐣 Easter  

---

## 🧠 Feature Engineering
Each city–holiday pair is represented using three feature groups:

### 1️⃣ Sentiment Features
- VADER compound sentiment (mean, std)
- Proportion of **positive / neutral / negative** reviews
- Average review length

### 2️⃣ Emotional Features (NRC Lexicon)
- 😊 Joy  
- 🤝 Trust  
- ⏳ Anticipation  
- 😢 Sadness  
- 😠 Anger  
- 😨 Fear  

### 3️⃣ Market Features
- Average nightly price  
- Price variability  
- Availability  
- Minimum stay  
- Number of listings  
- Proportion of entire-home listings  

📐 **All features were standardized prior to clustering.**

---

## ⚙️ Methodology
- **Model:** k-means clustering  
- **Approach:** Cities clustered independently per holiday 
- **Validation:**  
  - Silhouette Score  
  - Davies–Bouldin Index  
- **Visualization:** PCA (interpretability only)

A baseline sentiment-only clustering was compared against a richer feature set combining sentiment, emotion, and market data.

---

## 🔍 Key Findings
- Sentiment-only clustering produced high silhouette scores but limited interpretability.
- Rich feature clustering revealed stable and interpretable holiday experience profiles.
- Across all holidays, cities consistently separated into two main clusters:

### 🔥 High-Intensity Holiday Experiences
- Strong emotional signals  
- Premium pricing  
- High price variability  

### 🌿 Moderate / Stable Holiday Experiences
- Weaker emotional expression  
- Lower prices  
- Higher availability  

🧩 Emotional drivers varied by holiday  
(e.g., **joy & trust** for Valentine’s Day, **fear & anticipation** for Halloween),  
yet the **overall clustering structure remained consistent**.

---

## 🌍 Why This Matters
This project demonstrates that:
- High internal validation metrics alone can be misleading
- Multidimensional sentiment representations provide richer insight
- Unsupervised learning is powerful for exploratory tourism & urban analytics

The methodology generalizes to:
- Experience analysis  
- Market segmentation  
- Exploratory NLP tasks without labeled outcomes  

---

## 🛠️ Tools & Technologies
- Python
- pandas / NumPy  
- scikit-learn  
- VADER Sentiment Analysis  
- NRC Emotion Lexicon  
- PCA & k-means Clustering  

---


## 👤 Author
**Braum Russell**  
🎓 M.S. Data Science, Fordham University
