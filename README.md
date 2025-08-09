# 🎬 Movie Recommendation System – Content-Based & Collaborative Filtering

## 1. Problem Statement and Goal of Project

The goal of this project is to build a **movie recommendation system** using two core approaches:

1. **Content-Based Filtering** – Recommending movies similar to those a user already likes, based on movie attributes.
2. **Collaborative Filtering** – Recommending movies based on the preferences of users with similar tastes.

The project also explores the advantages and limitations of each method, with an intention to potentially combine them in a future **hybrid recommender system**.

---

## 2. Solution Approach

### **A. Content-Based Filtering**

* **Feature Extraction**

  * Extract movie release years from titles.
  * Split the `genres` column into individual genres.
  * Apply **One-Hot Encoding** to create binary genre columns (0 = not in genre, 1 = in genre).

* **User Profile Building**

  * Introduce an example user with predefined ratings.
  * Identify genres of rated movies and compute weighted scores for each genre based on user ratings.

* **Recommendation Generation**

  * Compare all movies’ genre vectors against the user’s weighted genre profile.
  * Rank movies by similarity score and recommend the top results.

* **Advantages & Limitations**

  * Strengths: Personalization, reduced cold start for new users, transparency in recommendations.
  * Weaknesses: Over-specialization, limited diversity, dependency on feature quality.

---

### **B. Collaborative Filtering**

* **User-Based Collaborative Filtering**

  * Find other users with similar rating patterns to the target user using historical ratings.
  * Recommend movies that similar users have rated highly and the target user hasn’t seen.

* **Advantages & Limitations**

  * Strengths: Can suggest unexpected items outside user’s known preferences, adaptable to changing tastes.
  * Weaknesses: Cold start problem, data sparsity, scalability issues, potential privacy concerns.

---

## 3. Technologies & Libraries

* **Python**
* **pandas** – Data manipulation and preprocessing
* **NumPy** – Numerical operations for profile and similarity calculations
* **Matplotlib** – Visualization of results (inline in Jupyter)

---

## 4. Description about Dataset

* **movies.csv** – Contains `movieId`, `title`, and `genres` for each movie.
* **ratings.csv** – Contains `userId`, `movieId`, `rating`, and `timestamp`.
* Timestamp is dropped for this implementation as it is not currently used in recommendation logic.

---

## 5. Installation & Execution Guide

1. **Clone the repository**:

   ```bash
   git clone <repo-url>
   cd <repo-folder>
   ```
2. **Install dependencies**:

   ```bash
   pip install pandas numpy matplotlib
   ```
3. **Run the notebook**:

   ```bash
   jupyter notebook "recommendation system project.ipynb"
   ```

---

## 6. Key Results / Performance

* **Content-Based Filtering** successfully recommends movies based on genre similarity to user preferences.
* **Collaborative Filtering** provides recommendations based on similar users’ ratings.
* The notebook contains step-by-step implementation and comparison of both methods.

---

## 7. Screenshots / Sample Outputs

Typical outputs in the notebook include:

* One-Hot Encoded genre matrix.
* Weighted genre profile for a sample user.
* Ranked list of recommended movies with highest similarity scores.
* Collaborative filtering recommendation lists.

---

## 8. Additional Learnings / Reflections

* Demonstrates a **clear understanding** of both content-based and collaborative filtering principles.
* Shows end-to-end preprocessing, feature engineering, and recommendation scoring without relying on pre-built recommender libraries.
* Highlights the trade-offs between the two methods and opens the path for future **hybrid recommender systems**.

---

## 👤 Author

**Mehran Asgari**
📧 [imehranasgari@gmail.com](mailto:imehranasgari@gmail.com)
🌐 [https://github.com/imehranasgari](https://github.com/imehranasgari)

---

## 📄 License

This project is licensed under the MIT License – see the `LICENSE` file for details.

---

> 💡 *Some interactive outputs (e.g., plots, widgets) may not display correctly on GitHub. If so, please view this notebook via [nbviewer.org](https://nbviewer.org) for full rendering.*

---
