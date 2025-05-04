# 🎥 YouTube Trending Video Extractor

This project fetches the **top 25 trending videos on YouTube** for a given region (default: US) using the **YouTube Data API v3** and saves the metadata to a local CSV file.

It's a lightweight, beginner-friendly data pipeline designed for quick exploration or to serve as a foundation for building a full ETL workflow.

---

## 📌 What It Does

- Authenticates with the **YouTube Data API**
- Fetches trending video data (`chart=mostPopular`)
- Extracts key video metadata including:
  - Title
  - Channel
  - Views, Likes, Comments
  - Tags, Category, Duration, etc.
- Saves the results to a **CSV file** (`trending_videos_enriched.csv`)

---

## 🧪 Sample Columns in Output

| Column           | Description                          |
|------------------|--------------------------------------|
| `video_id`       | Unique ID of the video               |
| `title`          | Video title                          |
| `channel_title`  | Channel name                         |
| `published_at`   | Video publish datetime               |
| `view_count`     | Total views                          |
| `like_count`     | Total likes                          |
| `comment_count`  | Total comments                       |
| `tags`           | List of tags (if available)          |
| `category_id`    | Category ID (can be mapped to name)  |
| `duration`       | Video length in ISO 8601 format      |
| `definition`     | HD or SD                             |
| `caption`        | Captions available or not            |
| `licensed_content` | Licensing info                     |
| `thumbnail_url`  | Link to video thumbnail              |

---

## 🚀 How to Run

1. **Install dependencies**
   ```bash
   pip install pandas requests

