# Spotify Trends & Popularity Analysis (230K Songs) 🎧

This project analyzes a large Spotify dataset (~230,000 songs) to understand what factors influence song popularity.
The complete workflow was done using **Excel, SQL, and Power BI** — starting from raw data cleaning to building an interactive dashboard.

---

## Project Objectives 🎯

- Identify the most popular genres on Spotify  
- Analyze artists with the highest number of hit songs  
- Study how audio features like energy, danceability, valence, and tempo affect popularity  
- Understand song distribution across popularity levels  
- Identify common characteristics of hit tracks  

---

## Tools & Technologies 🛠️

- **Excel** – Data cleaning and preprocessing  
- **SQL** – Data analysis and querying  
- **Power BI** – Dashboard creation and visualization  
- **DAX** – Custom measures and KPIs  

---

## Data Cleaning & Preparation 🧹

- Removed duplicate records  
- Handled missing and inconsistent values  
- Converted song duration from milliseconds to minutes  
- Created a `popularity_level` column (High / Medium / Low)  
- Standardized genre and artist names  
- Prepared the dataset for SQL analysis and Power BI  

---

## SQL Analysis 🧠

### Total Number of Songs
`SELECT COUNT(*) AS total_songs FROM spotifyclean;`

### Top 20 Most Popular Songs
`SELECT track_name, artist_name, popularity FROM spotifyclean ORDER BY popularity DESC LIMIT 20;`

### Genre-wise Average Popularity
`SELECT genre, AVG(popularity) AS avg_popularity FROM spotifyclean GROUP BY genre ORDER BY avg_popularity DESC;`

### Song Distribution by Popularity Level
`SELECT popularity_level, COUNT(*) AS total_songs FROM spotifyclean GROUP BY popularity_level;`

### Artists with the Most Hit Songs (Popularity ≥ 70)
`SELECT artist_name, COUNT(*) AS hit_count FROM spotifyclean WHERE popularity >= 70 GROUP BY artist_name ORDER BY hit_count DESC;`

---

## Power BI Dashboard 📊

### Visuals Included

- Total number of songs  
- Average popularity score  
- Average song duration  
- Popularity level distribution  
- Artists with the highest number of hit songs  
- Genre-wise popularity comparison  
- Energy vs danceability scatter plot  

### Filters & Slicers

- Artist  
- Genre  
- Popularity Level (High / Medium / Low)

---

## Key Insights 🔍

- Pop, Rap, and Rock genres have the highest average popularity  
- Artists like Drake, Ariana Grande, and The Weeknd frequently appear among hit tracks  
- High-popularity songs generally show higher energy and danceability  
- Most songs fall into Low and Medium popularity categories  
- The average song duration is approximately **3.9 minutes**

---

## Project Files 📁

- **Raw Dataset**  
  https://drive.google.com/file/d/1Et4ONScKN0TXuSmizuYEhhrC4gs_PV9i/view  

- **Cleaned Dataset**  
  https://docs.google.com/spreadsheets/d/1vTGuKV8w7Hzpg_7JbuFzAnn7MzKGKXaj/edit  

- **SQL Processed Data**  
  https://drive.google.com/file/d/1Nocta9j_3ZEIBLbn0Ub1cQHo1n09_osr/view  

- **Power BI Dashboard (PBIX)**  
  https://drive.google.com/file/d/1vxkS-JHMc8jHwFhMek87Jxsc7gWsRPJS/view  

- **Project Report (DOCX)**  
  https://docs.google.com/document/d/1cTLKUNE2wDZC8c-5jGuMtyYLQVl7Clbr/edit  

- **Presentation (PPT)**  
  https://drive.google.com/file/d/1A6xkk0yKHRMnWeGemkwpEClfK0TTBw71/view  

---

If you find this project useful, feel free to ⭐ the repository.

