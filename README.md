## 🎬 Movie Recommender System

This is a simple **Movie Recommendation Web App** built with **Streamlit** that recommends movies based on similarity using a **content-based filtering** approach. It uses **TMDB API** to fetch movie posters and metadata.

---

### 🚀 Features

* Recommend top 5 movies similar to the one selected
* Display movie posters fetched dynamically from **TMDB**
* Fast and responsive Streamlit-based UI
* Pre-trained similarity model using cosine similarity

---

### 📸 Demo
<img width="485" height="302" alt="image" src="https://github.com/user-attachments/assets/2ba95b4c-89be-4bf6-bab6-0fc48a8855f5" />




### 🧠 How It Works

1. Load precomputed movie list and similarity matrix using `pickle`.
2. Select a movie from the dropdown.
3. On clicking "Show Recommendation":

   * The app finds 5 most similar movies.
   * It fetches their posters via the **TMDB API**.
   * Shows the movie names and posters in a 5-column layout.

---

### 🛠️ Tech Stack

* 🐍 Python
* 📦 Streamlit
* 🧠 Pickle (Pre-trained similarity model)
* 🌐 TMDB API

---

### 📂 Project Structure

```
├── app.py                  # Streamlit App
├── model/
│   ├── movie_list.pkl      # Movie metadata
│   └── similarity.pkl      # Cosine similarity matrix
├── requirements.txt        # Python dependencies
└── README.md               # You're here!
```

---

### 🔐 Setup TMDB API Key

Replace the TMDB API key in `fetch_poster()` with your own.
Or use a secure method like:

```python
import os
api_key = os.getenv("TMDB_API_KEY")
```

Then set it locally or in `.env`.

---

### ✅ Installation

```bash
git clone https://github.com/yourusername/movie-recommender-app.git
cd movie-recommender-app

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py
```

---

### ☁️ Deploy on Streamlit Cloud

1. Push the repo to GitHub
2. Go to [Streamlit Cloud](https://streamlit.io/cloud)
3. Click "New App" → Connect your repo
4. Add `TMDB_API_KEY` to Secrets Manager
5. Done!

---

### 📄 Requirements

```txt
streamlit
requests
pickle5  # if needed for .pkl files
```

---

### 📌 To Do / Improvements

* 🔐 Secure API key via `st.secrets`
* 🔍 Add genre/category filtering
* 📱 Make layout mobile-responsive
* 📊 Add ratings or additional metadata
* 🌍 Add multilingual support (via TMDB)

---

### 📧 Contact

Made with ❤️ by [Tufan Dey](https://github.com/tufandey)
📩 Feel free to fork, star ⭐, or contribute!

