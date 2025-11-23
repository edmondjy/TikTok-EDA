## 📌 Project Overview
This project analyzes a dataset of **19,382 TikTok videos** to uncover trends in user engagement and content moderation. The primary goal was to understand the relationship between video content type ("Claim" vs. "Opinion") and engagement metrics (views, likes), as well as how these content types relate to author ban status.

**Key Business Question:** *How does the nature of the content (claims vs. opinions) impact user engagement and the risk of being banned?*

## 📂 Dataset
The dataset was sourced from [Ramin Huseyn](https://www.kaggle.com/datasets) and contains metadata for TikTok videos, including:
* **Video Metadata:** `video_duration_sec`, `video_transcription_text`
* **Engagement Metrics:** `video_view_count`, `video_like_count`, `video_share_count`, `video_download_count`
* **User Status:** `verified_status`, `author_ban_status`
* **Classification:** `claim_status` (Claim vs. Opinion)

## 🔑 Key Findings

### 1. Content Strategy: "Claims" vs. "Opinions"
There is a massive disparity in engagement between videos labeled as "claims" versus "opinions".
* **Claims:** Average **501,029 views** per video.
* **Opinions:** Average **4,956 views** per video.
* *Insight:* "Claim" videos (often viral or sensational content) drive **100x more traffic** than opinion-based content.

### 2. Moderation Risks (Ban Analysis)
High engagement comes with high risk. Authors posting "claim" content face significantly stricter moderation.
* **Claim Authors:** **31.6%** are either banned or under review.
* **Opinion Authors:** Only **6.9%** are banned or under review.
* *Insight:* While claims drive views, they are **4.5x more likely** to result in account restrictions compared to opinions.

### 3. Engagement Correlation
Engagement metrics are highly correlated.
* There is a strong positive correlation (**0.80**) between **Views** and **Likes**.
* If a video succeeds in one metric, it almost invariably succeeds in others (shares, downloads).

## 📊 Visualizations
Key visualizations generated in this project:
1.  **Distribution of Claim Status:** Shows the balance of the dataset.
2.  **Boxplot of Views by Status:** Highlights the massive engagement gap between claims and opinions.
3.  **Ban Status by Content Type:** Visualizes the higher risk associated with claim videos.
4.  **Correlation Heatmap:** Displays relationships between numerical engagement variables.

## 🛠️ Installation & Usage

### Prerequisites
Ensure you have Python installed. You will need the following libraries:
```bash
pip install pandas matplotlib seaborn
