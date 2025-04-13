# Netflix Movies and TV Shows Clustering 🎬

![Netflix Logo](https://upload.wikimedia.org/wikipedia/commons/0/08/Netflix_2015_logo.svg)

## Project Overview 📖

This project analyzes and clusters Netflix movies and TV shows available as of 2019, sourced from Flixable, a third-party Netflix search engine. The goal is to uncover insights about content trends and user preferences using unsupervised machine learning, specifically clustering, to build a recommendation system for an enhanced user experience.

**Project Type**: Unsupervised Machine Learning  
**Contributor**: Ankesh Aman  
**GitHub Repository**: [Netflix Movies and TV Shows Clustering](https://github.com/ankesh-aman/Netflix-Movies-And-TV-Shows-clustering) 🌐

---

## Problem Statement ❓

The dataset reveals a surge in TV shows (nearly tripled since 2010) and a decline in movies (over 2,000 fewer titles since 2010) on Netflix. This project aims to:

- Perform **Exploratory Data Analysis (EDA)** to uncover patterns in content distribution across countries, genres, and release trends 📊.
- Investigate Netflix's shift toward TV shows over movies 📺.
- Analyze content availability across different countries 🌍.
- Cluster similar content based on text features (e.g., descriptions, genres) to create a **recommendation system** for personalized experiences 🎯.

Integrating external datasets (e.g., IMDb, Rotten Tomatoes) could provide deeper insights, but this project focuses on the provided dataset.

---

## Dataset Description 📋

The dataset includes 12 features for each movie or TV show:

- **show_id**: Unique identifier 🆔.
- **type**: Movie or TV Show 🎥📺.
- **title**: Content title 📛.
- **director**: Director 🎬.
- **cast**: Actors involved 🎭.
- **country**: Production country 🌎.
- **date_added**: Date added to Netflix 📅.
- **release_year**: Release year 🗓️.
- **rating**: Content rating (e.g., TV-MA, PG-13) ⭐.
- **duration**: Duration in minutes (movies) or seasons (TV shows) ⏳.
- **listed_in**: Genre(s) 🏷️.
- **description**: Brief summary 📝.

---

## Methodology 🛠️

### 1. Data Preprocessing 🧹
- **Libraries Used**: Pandas, NumPy, NLTK, Scikit-learn, Matplotlib, Seaborn, Plotly, WordCloud 🐍.
- Handled missing values and cleaned text data (descriptions, genres) using tokenization, lemmatization, and stopword removal ✂️.
- Converted categorical features into numerical representations with **TF-IDF Vectorizer** for clustering 📈.

### 2. Exploratory Data Analysis (EDA) 🔍
- Analyzed content distribution by type, country, genre, and release trends.
- Visualized insights with bar plots, word clouds, and time-series graphs 📊🌥️.

### 3. Clustering 🧩
- **Algorithms Used**:
  - **K-Means Clustering**: Identified 4 optimal clusters based on text features 🔢.
  - **Agglomerative Hierarchical Clustering**: Found 2 optimal clusters 🌳.
- **Evaluation Metric**: **Silhouette Score** was chosen for its measure of cluster cohesion and separation, less sensitivity to cluster shape, and intuitive results 📏.
- **Feature Engineering**: Used TF-IDF vectors, reduced dimensionality with PCA for visualization 📉.

### 4. Recommendation System 🤝
- Built a system using **cosine similarity** to suggest similar movies or TV shows based on clustered content 🎥➡️📺.

---

## Key Insights from EDA 🔦

1. **Content Distribution** 📊:
   - Movies dominate, but TV show additions surged since 2018, while movies declined in 2020 vs. 2019 📺⬆️🎥⬇️.
   - **International Movies, Dramas, and Comedies** are top genres 😂🎭.

2. **Country-Specific Trends** 🌍:
   - **United States** leads, followed by **India** 🇺🇸🇮🇳.
   - **Japan** and **South Korea** focus on TV shows, showing growth potential 🇯🇵🇰🇷.
   - Spain produces significant **adult content**, Canada emphasizes **family-friendly** content 🇪🇸🇨🇦.

3. **Cast and Directors** 🎭:
   - Indian actors dominate movies, Japanese actors lead TV shows 🇮🇳🇯🇵.
   - **Jan Suter** is the top movie director, **Ken Burns** leads TV shows 🎬.

4. **Temporal Trends** 📅:
   - **October, November, December** are peak for TV shows; **January, October, November** for movies 🍂❄️.
   - **February** sees the least additions 📉.
   - Content is often added at the **start or middle of the month**, especially on **weekends** 🗓️.

5. **Content Duration** ⏳:
   - Movies: **80–120 minutes** 🎥.
   - TV shows: **1–2 seasons** 📺.

6. **Ratings** ⭐:
   - **Adult and teen** content prevails, with family-friendly content more common in TV shows 👨‍👩‍👧.

---

## Machine Learning Findings 🤖

- **K-Means Clustering** was chosen as the final model because:
  - Higher **Silhouette Score** than Hierarchical Clustering 📈.
  - Well-separated clusters in 3D PCA plots 🧩.
  - Scalability, speed, and ease of use for large datasets 🚀.
- Optimal clusters: **4 for K-Means**, **2 for Hierarchical Clustering** 🔢.
- The recommendation system uses cosine similarity to suggest content, enhancing user experience and reducing churn 🎯.
- Future enhancements could include external datasets (e.g., IMDb, Rotten Tomatoes) for richer recommendations 📚.

---

## Business Impact 💼

- **Enhanced User Experience**: Personalized recommendations increase engagement and satisfaction 😊.
- **Strategic Content Acquisition**: Insights guide Netflix’s production and acquisition strategies 🎬.
- **Reduced Churn**: Tailored suggestions improve retention 🔄.
- **Market Expansion**: Growth potential in Japan and South Korea informs global strategy 🌏.

---

## Technologies Used 💻

- **Programming**: Python 🐍
- **Libraries**: Pandas, NumPy, Scikit-learn, NLTK, Matplotlib, Seaborn, Plotly, WordCloud, Yellowbrick 📚
- **Tools**: Jupyter Notebook, Google Colab 📓
- **Techniques**: TF-IDF Vectorization, PCA, K-Means, Hierarchical Clustering, Cosine Similarity 🔧

---

## Future Scope 🚀

- Integrate datasets like IMDb ratings or Rotten Tomatoes for robust clustering 📊.
- Deploy the recommendation system as a web app for real-time interaction 🌐.
- Use advanced NLP (e.g., BERT embeddings) for better text clustering 🧠.
- Analyze user viewing patterns to refine recommendations 🔎.

---

Conclusion 🎉
This project showcases expertise in unsupervised machine learning, data preprocessing, and visualization, delivering actionable insights for Netflix’s content strategy. The clustering-based recommendation system enhances user experience, and the EDA reveals trends to inform business decisions. The project is extensible, with potential for external data integration and web deployment.
