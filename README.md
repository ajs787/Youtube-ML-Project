# **Youtube Viral Video Longevity**

---

### 👥 **Team Members**

| Name             | GitHub Handle | Contribution                                                             |
|------------------|---------------|--------------------------------------------------------------------------|
| Lakshita Madhavan   | @lakshita1212 | data exploration, model building & evaluating, project management (August 2025)        |
| Michelle Rahman   | @michelle-rahman   | feature selection, model building (Random Forest) & hyperparameter tuning, project management (September 2025) |
| Audrey Shin    | @ajs787  | data importing, environment setup, exploratory data analysis refinement, model building (XGBoost) & evaluating                  |
| Larry To     | @LarryTo      | feature engineering, model building (Logistic Regression) & hyperparameter tuning, project management (November 2025)  |
| Imandi Kathriarachchi      | @imandi01    | standardizing categorical variables, normalize numerical features, data splitting, model building (Support Vector Machine), project management (December 2025)            |
| Grace Yan      | @mengmenggy    | data exploration for different countries, model evalution     |
| Suman Bista      | @sumabista    | data understanding and preprocessing, model building (Decision Tree) & evaluating, project management (October 2025)          |



---

## 🎯 **Project Highlights**

* **Predictive ML Model**: Built a machine learning model to predict YouTube video virality using 321K videos from 11 countries. Compared 6 algorithms (KNN, Logistic Regression, Decision Tree, Random Forest, XGBoost, CatBoost) with Random Forest achieving best performance at 81.81% accuracy.

* **Feature Engineering**: Engineered meaningful features including engagement ratios (likes/views, comments/views), timing factors (day, hour, time-of-day categories), and viral lifespan metrics (days trending ≥ 7) to transform raw metadata into actionable insights.

* **Key Insights on Timing**: Discovered that morning video uploads have the highest likelihood of sustained virality, followed by nighttime and afternoon. Strong early engagement (high likes and comments-to-view ratios) significantly helps videos trend longer.

* **Content Strategy Findings**: Found that like-to-view ratio remains consistent (~6.3%) regardless of trending duration, suggesting creators should prioritize video duration and watch time over immediate likes for long-term success.

* **Future Improvements Identified**: Outlined clear next steps including NLP integration for content analysis (titles, descriptions, tags), topic modeling to identify trending themes, and incorporation of external factors like algorithm changes and viral social media trends.

---

## 👩🏽‍💻 **Setup and Installation**

* For the setup, we started by pulling the YouTube Trending Videos dataset from Kaggle and configuring a shared Google Colab notebook so the team could work in the same environment. In Colab, we connected our Google Drive, mounted the Kaggle files, and imported the CSVs directly into pandas so we could immediately explore and preprocess the data. To keep our work organized, we also created a shared Excel/Sheets tracker where we logged tasks, owners, and due dates for data cleaning, feature engineering, modeling, and presentation prep, which helped keep everyone aligned on priorities and progress.

## 🏗️ **Project Overview**


* **YouTube Viral Video Longevity**

* The goal of this project is to build a machine learning model that predicts whether a YouTube video will continue trending over time, rather than experiencing a short-lived spike in popularity. Using the YouTube Trending Video Dataset from Kaggle, we analyzed engagement metrics, video metadata, timing patterns, and regional information across 11 countries to better understand the drivers of sustained virality.

* We framed this as a binary classification problem, defining a video as continuing to trend if it remained on the trending page for seven or more days. Multiple machine learning models: including KNN, Logistic Regression, Decision Tree, Random Forest, XGBoost, CatBoost, and SVM were trained and evaluated using consistent preprocessing and performance metrics (accuracy, precision, recall, and F1 score).

* The final outcome is a comparative modeling framework that not only predicts long-term virality with strong performance, but also provides interpretable insights into what factors, such as early engagement strength, posting time, metadata richness, and regional context, most strongly influence how long a video stays trending. These insights are directly applicable to content creators, marketing strategists, and analytics teams seeking to optimize content strategy and timing.

---

## 🔍 Data Pipeline: Understanding & Preprocessing
### 1. Data Acquisition & Scope
To build a model capable of understanding **global viral mechanics**, we sourced daily trending video records from 11 distinct global markets.

* **Source:** [YouTube Trending Video Dataset (Kaggle)](https://www.kaggle.com/datasets/rsrishav/youtube-trending-video-dataset)
* **Scope:** 11 Regions (🇺🇸 US, 🇨🇦 CA, 🇬🇧 GB, 🇷🇺 RU, 🇩🇪 DE, 🇫🇷 FR, 🇯🇵 JP, 🇰🇷 KR, 🇮🇳 IN, 🇲🇽 MX, 🇧🇷 BR).
* **Sampling Strategy:** We applied **Stratified Sampling** (5,000 unique videos per country) to ensure equal representation and prevent high-volume markets like the US or India from biasing the model.

### 2. Dataset Schema
We consolidated 11 disparate CSV files into a unified schema containing **17 core features**.

| Feature Category | Columns |
| :--- | :--- |
| **Engagement Metrics** | `view_count`, `likes`, `dislikes`, `comment_count` |
| **Metadata** | `title`, `tags`, `description`, `categoryId`, `thumbnail_link` |
| **Temporal** | `publishedAt`, `trending_date` |
| **System Flags** | `comments_disabled`, `ratings_disabled` |
| **Identity** | `video_id`, `channelId`, `channelTitle`, `country_uniqueID` |

### 3. Data Cleaning
We performed a rigorous audit of the raw data (approx. 320,000 records) to ensure signal quality before modeling.

#### A. Handling Missing Values
* **Engagement Metrics:** We confirmed that critical numerical columns (`view_count`, `likes`, `dislikes`) contained **0 null values** across the entire dataset. This high data integrity allowed us to avoid aggressive imputation on target features.
* **Text Data:** The only column with significant missing data was `description` (~8,500 entries).
    * **Action:** Imputed missing values with empty strings (`""`).
    * **Reasoning:** To maintain consistency for NLP feature extraction and ensure the text fields remained valid strings for vectorization.

## 📊 **Data Exploration**

* 

---

## 🧠 **Model Development**
* For this project, each team member trained a different machine learning model to compare how well various algorithms could predict YouTube video virality. Our candidate models included Random Forest, KNN, Logistic Regression, Decision Tree, XGBoost, CatBoost, and SVM. All models followed the same preprocessing pipeline and were evaluated using accuracy, precision, recall, and F1 score. After running hyperparameter tuning and validating performance, the top three models were Random Forest, XGBoost, and Logistic Regression, which consistently delivered the strongest and most reliable results. These models were carried forward for deeper analysis in the results section.

---

## 📈 **Results & Key Findings**


* **🔍 Overall Model Performance**

To predict whether a YouTube video would continue trending for 7+ days, I trained and compared several machine learning models. All models used the same preprocessing pipeline and were evaluated using accuracy, precision, recall, and F1 score.

  * *🌲 Random Forest: ~0.82 accuracy*

  * *⚡ XGBoost: ~0.82 accuracy*

  * *🐱 CatBoost: ~0.82 accuracy*

  * *🌳 Decision Tree, KNN, SVM: ~0.75–0.76 range*

  * *📉 Logistic Regression: ~0.73 accuracy*

Based on both performance and stability, Random Forest, XGBoost, and CatBoost were selected as our primary models for interpretation.

* **⭐ Key Drivers of LongTerm Virality**

Across the best-performing models, the most important features were:

  * *🌍 country_uniqueID – strong regional differences in how long videos stay trending*

  * *📊 Engagement strength: view_count, likes, dislikes, comment_count*

  * *📈 Engagement ratios: likes_to_views_ratio, comments_to_views_ratio, dislikes_to_views_ratio*

  * *🏷️ Metadata richness: title_length, tags_length, number of tags*

  * *🕒 Posting patterns: published_hour, day of week, and time-of-day categories*

* **🧠 Takeaways**

Overall, the results suggest that virality persistence is not random. Early engagement, strong engagement ratios, thoughtful metadata, and regional context all meaningfully influence whether a video continues to trend over time.

---

## 🚀 **Next Steps**

* Incorporate textual features (titles, descriptions, tags) using NLP methods to improve prediction performance.
* Expand the dataset to include all nine available regions to increase model generalizability.
* Enhance feature engineering with sentiment analysis, topic modeling, and keyword extraction.
* Build a simple dashboard or visualization for creators to test video attributes and see predicted virality.

---

## 📝 **License**

Not applicable — the project is not open source.


---

## 📄 **References** 

Breiman, L. (2001). Random Forests. Machine Learning.

Chen, T., & Guestrin, C. (2016). XGBoost: A Scalable Tree Boosting System. Proceedings of the 22nd ACM SIGKDD.

Scikit-learn Developers. (2024). scikit-learn Documentation. https://scikit-learn.org

XGBoost Documentation. https://xgboost.readthedocs.io

Kaggle. YouTube Trending Videos Dataset


---

## 🙏 **Acknowledgements** 

We would like to give a special thanks to our 2025 Break Through Tech Fall AI studio coach Haziel Andrade as well our Google challenge advisors Steven Thon and Jonathan Li. 

