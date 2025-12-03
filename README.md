# **Youtube Viral Video Longevity**

---

### 👥 **Team Members**

| Name             | GitHub Handle | Contribution                                                             |
|------------------|---------------|--------------------------------------------------------------------------|
| Lakshita Madhavan   | @lakshita1212 | data exploration, model building & evaluating          |
| Michelle Rahman   | @michelle-rahman   | [contribution goes here] |
| Audrey Shin    | @ajs787  | [contribution goes here]                  |
| Larry To     | @LarryTo      | feature engineering, logistic regression, project management (November)  |
| Imandi Kathriarachchi      | @imandi01    | Standardizing categorical variables, normalize numerical features, Data Splitting            |
| Grace Yan      | @__    | [contribution goes here]            |
| Suman Bista      | @sumabista    | [contribution goes here]           |



---

## 🎯 **Project Highlights**


- 

---

## 👩🏽‍💻 **Setup and Installation**

* For the setup, we started by pulling the YouTube Trending Videos dataset from Kaggle and configuring a shared Google Colab notebook so the team could work in the same environment. In Colab, we connected our Google Drive, mounted the Kaggle files, and imported the CSVs directly into pandas so we could immediately explore and preprocess the data. To keep our work organized, we also created a shared Excel/Sheets tracker where we logged tasks, owners, and due dates for data cleaning, feature engineering, modeling, and presentation prep, which helped keep everyone aligned on priorities and progress.

## 🏗️ **Project Overview**

- 

---

## 📊 **Data Exploration**

* 

---

## 🧠 **Model Development**
* For this project, each team member trained a different machine learning model to compare how well various algorithms could predict YouTube video virality. Our candidate models included Random Forest, KNN, Logistic Regression, Decision Tree, XGBoost, CatBoost, and SVM. All models followed the same preprocessing pipeline and were evaluated using accuracy, precision, recall, and F1 score. After running hyperparameter tuning and validating performance, the top three models were Random Forest, XGBoost, and Logistic Regression, which consistently delivered the strongest and most reliable results. These models were carried forward for deeper analysis in the results section.

---

## 📈 **Results & Key Findings**


**🔍 Overall Model Performance**

To predict whether a YouTube video would continue trending for 7+ days, I trained and compared several machine learning models. All models used the same preprocessing pipeline and were evaluated using accuracy, precision, recall, and F1 score.

  *🌲 Random Forest: ~0.82 accuracy*

  *⚡ XGBoost: ~0.82 accuracy*

  *🐱 CatBoost: ~0.82 accuracy*

  *🌳 Decision Tree, KNN, SVM: ~0.75–0.76 range*

  *📉 Logistic Regression: ~0.73 accuracy*

Based on both performance and stability, Random Forest, XGBoost, and CatBoost were selected as our primary models for interpretation.

**⭐ Key Drivers of LongTerm Virality**

Across the best-performing models, the most important features were:

  *🌍 country_uniqueID – strong regional differences in how long videos stay trending*

  *📊 Engagement strength: view_count, likes, dislikes, comment_count*

  *📈 Engagement ratios: likes_to_views_ratio, comments_to_views_ratio, dislikes_to_views_ratio*

  *🏷️ Metadata richness: title_length, tags_length, number of tags*

  *🕒 Posting patterns: published_hour, day of week, and time-of-day categories*

**🧠 Takeaways**

Overall, the results suggest that virality persistence is not random. Early engagement, strong engagement ratios, thoughtful metadata, and regional context all meaningfully influence whether a video continues to trend over time.

---

## 🚀 **Next Steps**

**

---

## 📝 **License**



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

