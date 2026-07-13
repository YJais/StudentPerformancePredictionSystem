# 🎓 AI-Based Student Performance Prediction System

> **Hybrid Stacking Ensemble Learning | Streamlit | XGBoost | Scikit-learn | Plotly**

<p align="center">

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-Deployed-red?style=for-the-badge&logo=streamlit)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?style=for-the-badge&logo=scikitlearn)
![XGBoost](https://img.shields.io/badge/XGBoost-Ensemble-success?style=for-the-badge)
![Plotly](https://img.shields.io/badge/Plotly-Visualization-3f4f75?style=for-the-badge&logo=plotly)

</p>

---

# 🌐 Live Demo

### 🚀 Live Application

**https://studentperformancepredictionsystem-p.streamlit.app**

---

# 📖 Project Overview

The **AI-Based Student Performance Prediction System** is a Machine Learning application that predicts a student's **Final Exam Score** using a **Hybrid Stacking Ensemble Regression** model.

The project combines multiple regression algorithms to improve prediction accuracy and is deployed through an interactive **Streamlit Dashboard** featuring modern UI, real-time inference, personalized recommendations, and dynamic visualizations.

---

# 🎯 Problem Statement

Accurately predicting student academic performance helps educators identify students requiring additional academic support while enabling students to understand the impact of study habits and academic indicators on their final examination scores.

Traditional prediction methods often rely on a single machine learning algorithm, which may fail to capture both linear and non-linear relationships within educational datasets.

This project addresses this limitation by employing a **Hybrid Stacking Ensemble Learning** approach that combines multiple predictive models to improve overall prediction performance.

---

# ✨ Features

- Hybrid Stacking Ensemble Regression
- Real-Time Student Performance Prediction
- Premium Black & Gold Glassmorphism UI
- Dynamic Plotly Visualizations
- Personalized Study Recommendations
- Performance Categorization
- Responsive Dashboard
- Production-Ready Streamlit Deployment
- Clean and Modular Python Code

---

# 📊 Input Features

The prediction model uses the following academic indicators.

| Feature | Description | Range |
|----------|-------------|-------|
| Attendance | Student Attendance Percentage | 0 – 100% |
| Hours Studied | Average Daily Study Hours | 0 – 24 |
| Previous Scores | Previous/Internal Examination Score | 0 – 100 |
| Sleep Hours | Average Daily Sleep Duration | 0 – 12 |
| Tutoring Sessions | Number of Tutoring Sessions | 0 – 20 |

---

# 📈 Output

The application predicts:

- 🎯 Predicted Final Exam Score
- 🏆 Performance Category
- 💡 Personalized Recommendations
- 📊 Interactive Dashboard
- 📉 Dynamic Visualizations

---

# 🧠 Machine Learning Pipeline

```text
                    Student Inputs
                           │
                           ▼
                Data Preprocessing
                 (StandardScaler)
                           │
                           ▼
      ┌────────────────────────────────────┐
      │                                    │
      ▼                                    ▼
Linear Regression                 XGBoost Regressor
(Base Learner 1)                  (Base Learner 2)
      │                                    │
      └──────────────┬─────────────────────┘
                     ▼
         Linear Regression
            (Meta Learner)
          passthrough=True
                     │
                     ▼
       Predicted Final Exam Score
```

---

# ⚙️ Ensemble Learning Strategy

### Base Learners

- Linear Regression
- XGBoost Regressor

### Meta Learner

- Linear Regression

### Ensemble Technique

Stacking Regressor (`sklearn.ensemble.StackingRegressor`)

### Passthrough

Enabled (`passthrough=True`)

The meta learner receives:

- Predictions from Linear Regression
- Predictions from XGBoost
- Original Input Features

allowing it to learn from both model predictions and the original feature space.

---

# 📊 Visualizations

The dashboard provides interactive Plotly visualizations including:

- 📊 Feature Comparison Bar Chart
- 🎯 Predicted Score Gauge
- 🕸 Student Performance Radar Chart
- 📋 Prediction Summary Dashboard

All visualizations are generated dynamically using the user inputs and model prediction.

---

# 📂 Project Structure

```text
StudentPerformancePredictionSystem/
│
├── Dataset/
│
├── Notebook/
│
├── models/
│   ├── student_model.pkl
│   ├── scaler.pkl
│   └── features.pkl
│
├── Streamlit_App/
│   ├── app.py
│   ├── requirements.txt
│   └── assets/
│
├── Documentation/
│
└── README.md
```

---

# 💻 Technology Stack

| Layer | Technology |
|--------|------------|
| Programming Language | Python |
| Dashboard | Streamlit |
| Machine Learning | Scikit-learn |
| Ensemble Learning | XGBoost |
| Data Processing | Pandas, NumPy |
| Visualization | Plotly |
| Model Serialization | Pickle |

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/YJais/StudentPerformancePredictionSystem.git
```

Move into the project directory

```bash
cd StudentPerformancePredictionSystem
```

Install dependencies

```bash
pip install -r Streamlit_App/requirements.txt
```

---

# ▶️ Run the Application

```bash
streamlit run Streamlit_App/app.py
```

The application will be available at:

```
http://localhost:8501
```

---

# 📷 Application Screenshots

## 🏠 Home Dashboard

> *(Add Screenshot Here)*

---

## 📊 Prediction Dashboard

> *(Add Screenshot Here)*

---

## 📈 Interactive Charts

> *(Add Screenshot Here)*

---

## ℹ️ About Project

> *(Add Screenshot Here)*

---

# 📊 Model Performance

| Metric | Value |
|---------|-------|
| MAE | 1.2761 |
| MSE | 5.0817 |
| RMSE | 2.2543 |
| R² Score | 0.6405 |

---

# 🔮 Future Scope

- Batch Prediction using CSV Upload
- Student Authentication
- Prediction History
- Explainable AI (SHAP / LIME)
- REST API using FastAPI
- Database Integration
- Multi-language Support
- Mobile Responsive Dashboard
- Cloud-based Model Monitoring

---

# 🤝 Contributing

Contributions are welcome.

If you would like to improve this project:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a Pull Request

---

# 👨‍💻 Developer

## **Yash Raj Jaiswal**

**B.Tech Computer Science & Engineering**

Machine Learning • Artificial Intelligence • Full Stack Development

### GitHub

https://github.com/YJais

### LinkedIn

https://www.linkedin.com/in/yashraj27/

---

# 📚 Acknowledgements

- Scikit-learn
- XGBoost
- Streamlit
- Plotly
- Pandas
- NumPy
- Kaggle Student Performance Factors Dataset

---

# 📄 License

This project is developed for educational, research, and demonstration purposes.

---

⭐ If you found this project useful, consider giving it a **Star** on GitHub!
