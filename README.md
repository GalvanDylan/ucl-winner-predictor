# ⚽ Predicting the 2025 UEFA Champions League Winner Using FIFA-Based Machine Learning

This project uses **FIFA video game player statistics** and UEFA Champions League (UCL) team rosters to train a machine learning model that forecasts the most likely winner of the **2024–25 UCL season**. The system combines sports analytics, ensemble learning, and probabilistic simulations to predict the tournament outcome with real-world validation from previous seasons.

---

## 🎯 Objective

To determine whether player attribute data from the FIFA game series — such as overall rating, pace, shooting, passing, and physicality — can be used to **predict the outcome of the UEFA Champions League**, using machine learning and historical season analysis.

---

## 🧠 Methodology

### 🔍 Data Sources
- Player attributes from FIFA 21–25 via Kaggle
- Club rosters from UCL 2021–2025 (manually curated)
- Ground-truth champion labels for 2021–2024 seasons

### 🛠 Preprocessing
- Standardized inconsistent columns across multiple FIFA datasets
- Grouped player data by club to extract:
  - Mean team stats (`avg_*`)
  - Top 5 player averages (`top5_avg_*`)
  - Roster size
- Built consistent, labeled team-level feature datasets for each season

### 🧪 Model Training
- Combined seasons 2021–2024 into a training dataset
- Used `RandomForestClassifier` with `RandomizedSearchCV` for hyperparameter optimization
- Features included: `avg_overall`, `avg_pac`, `top5_avg_sho`, `top5_avg_phy`, etc.

### 🔄 Tournament Simulation
- Built 2025 season features from FIFA 25 stats
- Modeled the four 2025 semifinalist teams: Arsenal, Barcelona, Paris SG, Lombardia FC (Inter Milan)
- Used trained model to predict winner based on learned patterns

---

## 📈 Results

- **Model Validation:** Correctly predicted or closely ranked top clubs in 2021–2024 seasons
- **2025 Semifinals Prediction:**
  - **Predicted Winner:** Lombardia FC (Inter Milan)
  - **Prediction Confidence:** Displayed via probability score from the trained model

---

## 🛠 Tools & Libraries

| Tool           | Purpose                            |
|----------------|-------------------------------------|
| **Python**     | Main language                      |
| **pandas**     | Data cleaning, grouping, merging   |
| **NumPy**      | Numerical operations               |
| **scikit-learn** | Modeling, hyperparameter tuning   |
| **matplotlib / seaborn** | Visualization             |
| **KaggleHub**  | Dataset integration from Kaggle    |
| **Google Colab** | Cloud-based development notebook |

---

## ▶️ Run in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1d5HSj7MYwBYs2bqfnN3d5pcbM-OLbKB9?usp=sharing)


---

## 🔮 Future Improvements

- Expand to full 32-team simulation and predict bracket outcomes
- Integrate match fitness or live stats using real-time APIs
- Add explainability using SHAP or feature importance visualizations
- Deploy as a **web app** using Streamlit or Flask





