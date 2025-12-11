# 🎵 Spotify Trends & Popularity Analysis Dashboard
Unlocking insights from **230K+ songs** using **Excel → SQL → Power BI** ⚡

---

## 📌 Project Summary

This project analyzes Spotify’s large-scale song dataset to uncover:

- Which genres are most popular  
- Which artists produce the most hit songs  
- How audio features (energy, danceability, valence, tempo) influence popularity  
- Popularity distribution across songs  
- Characteristics that define a “hit” track  

The workflow includes **data cleaning**, **SQL analysis**, and a fully interactive **Power BI dashboard**.

---

## 🛠 Tech Stack

| Tool      | Purpose |
|-----------|---------|
| Excel     | Cleaning & preprocessing |
| SQL       | Data analysis & querying |
| Power BI  | Dashboard creation |
| DAX       | Custom measures |

---

## 🧹 Data Cleaning Steps

- Removed duplicate rows  
- Handled missing values  
- Converted duration from ms → minutes  
- Added `popularity_level` (High / Medium / Low)  
- Cleaned genres & artist names  
- Prepared dataset for SQL + BI  

---

## 🧠 Key SQL Queries Used

### ⭐ Total Songs
```sql
SELECT COUNT(*) AS total_songs FROM spotifyclean;
```

### ⭐ Top 20 Most Popular Songs
```sql
SELECT track_name, artist_name, popularity
FROM spotifyclean
ORDER BY popularity DESC
LIMIT 20;
```

### ⭐ Most Popular Genre
```sql
SELECT genre, AVG(popularity) AS avg_popularity
FROM spotifyclean
GROUP BY genre
ORDER BY avg_popularity DESC;
```

### ⭐ Song Distribution by Popularity Level
```sql
SELECT popularity_level, COUNT(*) AS total_songs
FROM spotifyclean
GROUP BY popularity_level;
```

### ⭐ Artists With Most Hit Songs (popularity ≥ 70)
```sql
SELECT artist_name, COUNT(*) AS hit_count
FROM spotifyclean
WHERE popularity >= 70
GROUP BY artist_name
ORDER BY hit_count DESC;
```

---

## 📊 Power BI Dashboard Highlights

### 🔥 Visuals Created
- Total Songs  
- Average Popularity Score  
- Average Duration  
- Popularity Level Distribution (Pie Chart)  
- Most Streamed Artists (Hit Song Count)  
- Genre-wise Popularity  
- Energy vs Danceability Scatter Plot  

### 🎛 Slicers Added
- Artist  
- Genre  
- Popularity Level (High, Medium, Low)

---

## 🚀 Insights Discovered

- Pop, Rap & Rock dominate popularity  
- Drake, Ariana Grande & The Weeknd appear among top hit-song artists  
- High-popularity tracks show strong energy + danceability  
- Majority of songs fall into Low & Medium popularity brackets  
- Average song duration ≈ **3.9 minutes**

---

## 🌟 Why This Project Stands Out

- End-to-end data analytics workflow  
- Real-world dataset (230K+ rows)  
- SQL + Power BI integration  
- Clean & interactive visuals  
- Strong portfolio/value for resumes  

---

## 📁 Project Files (Download Links)

All large files are hosted on Google Drive:

- **Dataset (Raw):**  
  https://drive.google.com/file/d/1Et4ONScKN0TXuSmizuYEhhrC4gs_PV9i/view?usp=sharing

- **Cleaned Dataset:**  
  https://docs.google.com/spreadsheets/d/1vTGuKV8w7Hzpg_7JbuFzAnn7MzKGKXaj/edit?usp=sharing

- **SQL Processed Data:**  
  https://drive.google.com/file/d/1Nocta9j_3ZEIBLbn0Ub1cQHo1n09_osr/view?usp=sharing

- **Project Report (DOCX):**  
  https://docs.google.com/document/d/1cTLKUNE2wDZC8c-5jGuMtyYLQVl7Clbr/edit?usp=sharing

- **Power BI Dashboard (PBIX):**  
  https://drive.google.com/file/d/1vxkS-JHMc8jHwFhMek87Jxsc7gWsRPJS/view?usp=sharing

- **Presentation (PPT):**  
  https://drive.google.com/file/d/1A6xkk0yKHRMnWeGemkwpEClfK0TTBw71/view?usp=sharing

---
 
If you like the project, ⭐ the repository.  
ThankkkYoU !

