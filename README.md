🎵 Spotify Trends & Popularity Analysis Dashboard

Unlocking insights from 230K+ songs using SQL, Excel & Power BI ⚡

📌 Project Summary

This project dives deep into Spotify’s massive song dataset to uncover:
✔ Which genres are most popular
✔ Which artists produce the most hit songs
✔ How audio features (energy, danceability, valence) relate to popularity
✔ How popularity is distributed across songs
✔ Which characteristics define a “hit” track

Everything was cleaned, analyzed, and visualized using Excel → SQL → Power BI.

🛠 Tech Stack
Tool	Use Case
Excel	Cleaning, preprocessing
SQL	Analysis & querying insights
Power BI	Dashboard & visuals
DAX	Custom measures (Hit Songs, Averages, etc.)
🧹 Data Cleaning Steps

✔ Removed duplicates
✔ Handled missing values
✔ Converted duration → minutes
✔ Created popularity_level (High / Medium / Low)
✔ Cleaned genres & artist names
✔ Prepared dataset for SQL & BI

🧠 Key SQL Queries Used
⭐ Total Songs
SELECT COUNT(*) AS total_songs FROM spotifyclean;

⭐ Top 20 Most Popular Songs
SELECT track_name, artist_name, popularity
FROM spotifyclean
ORDER BY popularity DESC
LIMIT 20;

⭐ Most Popular Genre
SELECT genre, AVG(popularity) AS avg_popularity
FROM spotifyclean
GROUP BY genre
ORDER BY avg_popularity DESC;

⭐ Song Distribution by Popularity Level
SELECT popularity_level, COUNT(*) AS total_songs
FROM spotifyclean
GROUP BY popularity_level;

⭐ Artists With Most Hit Songs (popularity ≥ 70)
SELECT artist_name, COUNT(*) AS hit_count
FROM spotifyclean
WHERE popularity >= 70
GROUP BY artist_name
ORDER BY hit_count DESC;

📊 Power BI Dashboard Highlights
🔥 Visuals Created

Total Songs Available

Average Popularity Score

Average Song Duration

Song Distribution by Popularity Level (Pie Chart)

Most Streamed Artists (By Hit Songs Count)

Genre-Wise Average Popularity

Energy vs Danceability Scatter Plot (Characteristics of Hit Songs)

🎛 Slicers Added

Artist Name

Genre

Popularity Level (High, Medium, Low)

🚀 Insights Discovered

🎧 Pop, Rap & Rock dominate popularity
🔥 Drake, Ariana Grande & The Weeknd appear as top hit-song artists
💥 High-popularity songs show high energy + high danceability
🎭 Most songs fall into Low & Medium popularity ranges
⏳ Average song duration is around 3.9 minutes

⭐ Why This Project Stands Out

Shows end-to-end analytics workflow

Uses real-world data (230k+ rows)

Powerful SQL + BI combo

Clean, professional interactive dashboard

Excellent for resume + portfolio + interviews


(files) 👇

Dataset : https://drive.google.com/file/d/1Et4ONScKN0TXuSmizuYEhhrC4gs_PV9i/view?usp=sharing
Cleaned Dataset : https://docs.google.com/spreadsheets/d/1vTGuKV8w7Hzpg_7JbuFzAnn7MzKGKXaj/edit?usp=sharing&ouid=113751015016733130879&rtpof=true&sd=true
SQL Processed Data : https://drive.google.com/file/d/1Nocta9j_3ZEIBLbn0Ub1cQHo1n09_osr/view?usp=sharing
Project Report : https://docs.google.com/document/d/1cTLKUNE2wDZC8c-5jGuMtyYLQVl7Clbr/edit?usp=sharing&ouid=113751015016733130879&rtpof=true&sd=true
Dashboard : https://drive.google.com/file/d/1vxkS-JHMc8jHwFhMek87Jxsc7gWsRPJS/view?usp=sharing
Presentation : https://drive.google.com/file/d/1A6xkk0yKHRMnWeGemkwpEClfK0TTBw71/view?usp=sharing

Made with ♥
If you like the project, ⭐ the repo ThankkkkYou !
