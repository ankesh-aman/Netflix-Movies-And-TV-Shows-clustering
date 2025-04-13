# Netflix Movies and TV Shows Clustering

![Netflix Logo](https://upload.wikimedia.org/wikipedia/commons/0/08/Netflix_2015_logo.svg)

## Project Overview

This project focuses on analyzing and clustering Netflix movies and TV shows available as of 2019, sourced from Flixable, a third-party Netflix search engine. The primary goal is to uncover insights about content distribution, trends, and user preferences using unsupervised machine learning techniques, specifically clustering, to enhance the user experience through a recommendation system.

**Project Type**: Unsupervised Machine Learning  
**Contributor**: Ankesh Aman  
**GitHub Repository**: [Netflix Movies and TV Shows Clustering](https://github.com/ankesh-aman/Netflix-Movies-And-TV-Shows-clustering)

---

## Problem Statement

The dataset provides a snapshot of Netflix's content library, highlighting a significant increase in TV shows (nearly tripled since 2010) and a decrease in movies (over 2,000 fewer titles since 2010). This project aims to:

- Perform **Exploratory Data Analysis (EDA)** to uncover patterns in content distribution across countries, genres, and release trends.
- Investigate whether Netflix has shifted focus toward TV shows over movies.
- Understand content availability across different countries.
- Cluster similar content based on text-based features (e.g., descriptions, genres) to build a **recommendation system** for personalized user experiences.

Additionally, integrating external datasets (e.g., IMDb ratings, Rotten Tomatoes) could yield deeper insights, though this project focuses on the provided dataset.

---

## Dataset Description

The dataset contains 12 features for each movie or TV show:

- **show_id**: Unique identifier for each title.
- **type**: Movie or TV Show.
- **title**: Title of the content.
- **director**: Director of the content.
- **cast**: Actors involved.
- **country**: Country of production.
- **date_added**: Date when added to Netflix.
- **release_year**: Actual release year.
- **rating**: Content rating (e.g., TV-MA, PG-13).
- **duration**: Duration in minutes (movies) or seasons (TV shows).
- **listed_in**: Genre(s) of the content.
- **description**: Brief summary of the content.

---

## Methodology

### 1. Data Preprocessing
- **Libraries Used**: Pandas, NumPy, NLTK, Scikit-learn, Matplotlib, Seaborn, Plotly, WordCloud.
- Handled missing values and cleaned text data (e.g., descriptions, genres) using techniques like tokenization, lemmatization, and stopword removal.
- Converted categorical features into numerical representations using **TF-IDF Vectorizer** for text-based clustering.

### 2. Exploratory Data Analysis (EDA)
- Analyzed content distribution by type (movies vs. TV shows), country, genre, and release trends.
- Visualized insights using bar plots, word clouds, and time-series graphs to identify patterns.

### 3. Clustering
- **Algorithms Used**:
  - **K-Means Clustering**: Identified optimal clusters (k=4) based on text features.
  - **Agglomerative Hierarchical Clustering**: Found optimal clusters (k=2).
- **Evaluation Metric**: **Silhouette Score** was chosen over distortion score because it measures both cluster cohesion and separation, is less sensitive to cluster shape, and provides intuitive results.
- **Feature Engineering**: Combined text features (descriptions, genres) into TF-IDF vectors, reduced dimensionality using PCA for visualization.

### 4. Recommendation System
- Built a recommendation system using **cosine similarity** on clustered content to suggest similar movies or TV shows based on user preferences.

---

## Key Insights from EDA

1. **Content Distribution**:
   - Movies dominate Netflix's library, but TV show additions have surged since 2018, while movie additions declined in 2020 compared to 2019.
   - **International Movies, Dramas, and Comedies** are the most popular genres.

2. **Country-Specific Trends**:
   - The **United States** leads in content production, followed by **India**.
   - **Japan** and **South Korea** produce more TV shows than movies, indicating growth potential.
   - Spain contributes significantly to **adult content**, while Canada focuses on **family-friendly** content.

3. **Cast and Directors**:
   - Indian actors dominate movies, but are absent from TV shows, where Japanese actors prevail.
   - **Jan Suter** is the most frequent movie director, and **Ken Burns** leads for TV shows.

4. **Temporal Trends**:
   - **October, November, and December** see high TV show additions; **January, October, and November** for movies. **February** has the least additions.
   - Content is typically added at the **start or middle of the month**, often on **weekends**.

5. **Content Duration**:
   - Movies typically last **80–120 minutes**.
   - TV shows commonly have **1–2 seasons**.

6. **Ratings**:
   - **Adult and teen** content is prevalent, with family-friendly content more common in TV shows than movies.

---

## Machine Learning Findings

- **K-Means Clustering** was selected as the final model due to:
  - Higher **Silhouette Score** compared to Agglomerative Hierarchical Clustering.
  - Well-separated clusters visualized in 3D PCA plots.
  - Scalability, speed, and ease of use for large datasets.
- Optimal clusters: **4 for K-Means**, **2 for Hierarchical Clustering**.
- The recommendation system leverages cosine similarity to suggest content, improving user experience and potentially reducing subscriber churn.
- Future enhancements could integrate external datasets (e.g., IMDb, Rotten Tomatoes) for richer recommendations.

---

## Business Impact

- **Enhanced User Experience**: The clustering-based recommendation system personalizes content suggestions, increasing user engagement and satisfaction.
- **Strategic Content Acquisition**: Insights into country-specific trends and genre popularity guide Netflix's content production and acquisition strategies.
- **Reduced Churn**: Personalized recommendations can improve retention by aligning content with user preferences.
- **Market Expansion**: Identifying growth potential in regions like Japan and South Korea informs Netflix's global strategy.

---

## Technologies Used

- **Programming**: Python
- **Libraries**: Pandas, NumPy, Scikit-learn, NLTK, Matplotlib, Seaborn, Plotly, WordCloud, Yellowbrick
- **Tools**: Jupyter Notebook, Google Colab
- **Techniques**: TF-IDF Vectorization, PCA, K-Means, Hierarchical Clustering, Cosine Similarity

---

## Future Scope

- Integrate external datasets (e.g., IMDb ratings, Rotten Tomatoes, book adaptations) for more robust clustering and recommendations.
- Deploy the recommendation system as a web application for real-time user interaction.
- Explore advanced NLP techniques (e.g., BERT embeddings) for improved text-based clustering.
- Analyze user viewing patterns to refine recommendations further.

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/ankesh-aman/Netflix-Movies-And-TV-Shows-clustering.git
