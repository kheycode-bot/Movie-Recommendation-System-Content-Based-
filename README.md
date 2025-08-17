# 🎬 Movie Recommendation System (Content-Based)
A Streamlit-based movie recommender system built with Python that uses content-based filtering and cosine similarity to suggest movies similar to a selected title, enhanced with real-time poster fetching via the TMDB API.
---

## 🔍 Types of Recommendation Systems

### 1. Content-Based Filtering
- Recommends items that are similar to those the user liked before.
- Works by analyzing item features like genre, cast, description, etc.
- Example: If you like *Inception*, it recommends movies with similar genres or directors.

### 2. Collaborative Filtering
- Recommends items that other users with similar tastes liked.
- Based on user behavior and interaction (e.g., ratings).
- Doesn’t care about the content of the items.

### 3. Hybrid Methods
- Combine both content-based and collaborative filtering.
- Aim to improve accuracy by using the strengths of both approaches.

---

## ⚙️ How This System Works (Back-End Logic)

### 1. Dataset
- We use a dataset containing movie details such as:
  - Title
  - Genre
  - Keywords
  - Overview (description)
  - Cast and Crew

### 2. Feature Engineering
- We combine multiple columns (like genres, keywords, etc.) into a single text string for each movie.
- This combined text is used to understand the "content" of a movie.

### 3. Text Vectorization
- We convert the combined text into numerical vectors using **CountVectorizer** or **TF-IDF**.
- Each movie becomes a vector in multi-dimensional space.

### 4. Similarity Measurement
- We calculate the **cosine similarity** between all movie vectors.
- When a user selects a movie, we find the top 10 most similar movies based on cosine similarity scores.

### 5. Movie Posters
- We fetch movie posters using the **TMDB API**.
- Posters are displayed alongside recommendations using Streamlit.

---
