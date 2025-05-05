# netflix-recommendation

# 🎬 Netflix Movie Recommendation System

This project builds a personalized movie recommendation system based on user behavior and collaborative filtering techniques. Inspired by real-world platforms like Netflix and Bumble, it focuses on enhancing user engagement by suggesting relevant movies using machine learning models trained on large-scale user-item interaction data.

---

## 📌 Problem Statement

With millions of movies and user interactions, users often face decision fatigue when choosing what to watch next. The objective of this project is to predict how a user would rate a movie they haven’t watched yet — and to recommend the most relevant titles — by analyzing historical user-movie rating patterns. This recommendation logic simulates matchmaking and content personalization systems used in real platforms.

---

## 📂 Dataset

- **Source:** Netflix Prize Dataset (or similar MovieLens-style format)
- **Volume:** Over 5 million user-movie rating entries
- **Fields Used:**
  - `UserID`: Anonymized user ID
  - `MovieID`: Movie identifier
  - `Rating`: Rating given by user (1–5 scale)
  - `Timestamp`: (Optional) time of rating

---

## 🧠 Approach & Methodology

### 1. **Data Cleaning & Exploration**
- Removed users/movies with very few ratings to ensure modeling robustness
- Visualized distribution of ratings, user activity, and top-rated movies
- Identified sparsity and challenges in user-item matrix

### 2. **Modeling Techniques**
- **Collaborative Filtering:**  
  Used matrix factorization (SVD) from the `Surprise` library to learn latent features of users and items
- **Model Benchmarks:**
  - `SVD` (Singular Value Decomposition)
  - `KNNBasic` (item-item collaborative filtering)
  - `BaselineOnly` (user/item mean rating)
  - `NormalPredictor` (random baseline)

### 3. **Evaluation**
- Applied **RMSE (Root Mean Square Error)** to measure prediction accuracy
- Achieved an **RMSE of 0.91**, improving accuracy by **12% over baseline models**
- Visualized actual vs. predicted ratings to assess performance

---

## 💡 Business & Product Impact

- 📈 **Improved Recommendation Relevance:** Enhances personalized user experience by showing high-likelihood movies
- ⏱️ **Reduced Friction:** Helps users quickly discover content they’re likely to enjoy
- 🧠 **Scalable Logic:** Mirrors how large platforms like Netflix, Spotify, and Bumble personalize content using user interactions

---

## 🛠️ Tech Stack

| Category            | Tools & Libraries                            |
|---------------------|----------------------------------------------|
| Data Manipulation   | Python, Pandas, NumPy                        |
| Modeling            | Surprise (SVD, KNN, Baseline), Scikit-learn |
| Visualization       | Matplotlib, Seaborn                          |
| Evaluation          | RMSE, MAE, Cross-Validation                  |
| (Optional) Pipeline | FastAPI, Flask (for deployment)              |

---

## 📊 Sample Output

| User ID | Recommended Movies          | Predicted Rating |
|---------|-----------------------------|------------------|
| 123     | The Matrix, Inception, Shrek| 4.7, 4.6, 4.5     |
| 456     | Titanic, Avatar, Gladiator  | 4.8, 4.6, 4.4     |

> These recommendations were generated based on similar users’ preferences and past behavior.

---

## 🚀 Future Improvements

- Add **content-based filtering** using genres, cast, and keywords
- Blend models using **hybrid recommendation systems**
- Deploy as a REST API using **FastAPI or Flask**
- Build a **frontend interface** to simulate Netflix-like movie browsing
- Implement **implicit feedback** models based on watch time instead of just ratings

---

## 🧑‍💻 Author

**Pratikkumar [Your Last Name]**  
Postgraduate Diploma in Business Analytics – Warwick Business School  
Email: [your-email@example.com]  
LinkedIn: [linkedin.com/in/your-profile](#)

---

## 📄 License

This project is released under the [MIT License](LICENSE). You are free to reuse and extend this work with attribution.

---

## 🙌 Acknowledgments

- Netflix Prize Dataset
- Surprise Recommendation Library by Nicolas Hug
- Scikit-learn, Matplotlib, and the open-source community

