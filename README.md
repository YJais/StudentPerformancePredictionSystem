# 🎓 AI-Based Student Performance Prediction System

### Hybrid Stacking Ensemble Learning · Streamlit · Plotly · XGBoost

A premium, production-ready AI dashboard that predicts a student's final
exam score using a **Hybrid Stacking Regressor** (Linear Regression +
XGBoost → Linear Regression meta-learner), presented through a modern
black & gold glassmorphism interface.

---

## 📖 Project Description

This system predicts a student's **Final Exam Score** based on three key
academic indicators:

| Feature | Range |
|---|---|
| Attendance (%) | 0 – 100 |
| Hours Studied (per day) | 0 – 24 |
| Previous / Internal Score | 0 – 100 |

The trained model is loaded from disk (`student_model.pkl` /
`scaler.pkl`) and used **purely for inference** — no retraining happens
inside the Streamlit application.

The app returns:

- ✅ Predicted Exam Score
- ✅ Performance Category (Outstanding → Needs Improvement)
- ✅ Natural-language Confidence Message
- ✅ Personalized Recommendations
- ✅ Four interactive Plotly visualizations (Bar, Gauge, Radar, Pie)

---

## 🧬 Machine Learning Pipeline

```
Student Inputs
      ↓
Preprocessing (StandardScaler)
      ↓
Linear Regression   ─┐
                      ├──►  Linear Regression (Meta Learner)
XGBoost Regressor   ─┘
      ↓
Predicted Exam Score
```

**Base Learners:** Linear Regression, XGBoost Regressor
**Meta Learner:** Linear Regression
**Ensembling Strategy:** Stacking (`sklearn.ensemble.StackingRegressor`)

Model performance on held-out synthetic test data: **R² ≈ 0.92**, **MAE ≈ 3.6 marks**.

---

## 🗂️ Project Structure

```
student-performance/
│
├── app.py                # Streamlit inference application (main entry point)
├── train_model.py        # Offline training script (produces the .pkl artifacts)
├── student_model.pkl     # Pre-trained Hybrid Stacking Regressor
├── scaler.pkl            # Fitted StandardScaler
├── requirements.txt      # Python dependencies
├── assets/
│   └── images/           # Static image assets
└── README.md             # Project documentation
```

---

## ⚙️ Installation

1. **Clone / extract the project**
   ```bash
   cd student-performance
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

---

## ▶️ Run Commands

**Run the Streamlit dashboard:**
```bash
streamlit run app.py
```

The app will open automatically at `http://localhost:8501`.

**(Optional) Regenerate the model artifacts:**
```bash
python train_model.py
```
This regenerates `student_model.pkl` and `scaler.pkl` from a fresh
training run. The Streamlit app never needs to run this — it only
loads the existing pickle files.

---

## 🖼️ Screenshots

> _Add screenshots of the running dashboard here._

- `assets/images/hero.png` — Hero / landing section
- `assets/images/result.png` — Prediction result & score card
- `assets/images/charts.png` — Visualization dashboard
- `assets/images/about.png` — About project page

---

## 🛠️ Technology Stack

| Layer | Technology |
|---|---|
| Frontend / Dashboard | Streamlit (custom black & gold glassmorphism CSS) |
| Visualization | Plotly (Bar, Gauge, Radar, Pie charts) |
| Machine Learning | Scikit-learn, XGBoost |
| Model Serialization | Pickle |
| Language | Python 3.10+ |

---

## ✨ Features

- Premium dark-themed, glassmorphic dashboard UI with subtle animations
- Real-time inference using a pre-trained Hybrid Stacking Ensemble
- Automatic performance categorization (6 tiers)
- Personalized, rule-based recommendations
- Four rich interactive Plotly visualizations
- Sidebar navigation: Predict / About Project / Developer Info
- Structured JSON-style backend response viewer
- Fully cached model loading for fast repeated predictions
- Clean, type-hinted, modular, production-ready Python code

---

## 🔭 Future Scope

- Integrate a real, larger-scale historical student dataset
- Add authentication and per-student prediction history tracking
- Support batch predictions via CSV upload
- Add SHAP-based model explainability visualizations
- Deploy as a REST API (FastAPI) alongside the Streamlit UI
- Add multi-language support for the recommendation engine
- Introduce time-series tracking of a student's performance trend

---

## 📜 License

This project is provided for educational and demonstration purposes.
