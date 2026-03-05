# 🎓 Student Engagement Risk Prediction & Recommendation System

A machine learning powered system that detects **early academic risk** based on student engagement behavior and provides **personalized study recommendations**.

This project demonstrates how to move from **ML experimentation → real ML product** by combining feature engineering, model inference, explainable AI, recommendations, and a deployed web application.

---

# 🚀 Live Demo

Streamlit App  
https://student-engagement-risk-prediction-recommendation-system.streamlit.app

---

# 📌 Problem Statement

In many online learning platforms and universities, students who eventually fail often show **early disengagement patterns** such as:

- Late course start
- Low early interaction
- Inconsistent engagement
- Minimal interaction with learning materials

However, intervention usually happens **too late**.

### Goal

Build a system that:

1️⃣ Detects **early academic risk**  
2️⃣ Explains **why the risk exists**  
3️⃣ Provides **actionable recommendations**

---

# 🧠 Solution Overview

The system analyzes **student behavioral engagement signals** and predicts the probability that a student may be at academic risk.

Instead of simply predicting success or failure, the system focuses on **early risk detection** and **recommended corrective actions**.

### Core Idea

```
Student Behavior Data
        ↓
Feature Engineering
        ↓
Machine Learning Model
        ↓
Risk Prediction
        ↓
Explainable AI
        ↓
Personalized Recommendations
```

---

# 📊 Features Used

The model uses behavioral engagement signals such as:

| Feature | Description |
|------|------|
| `total_click` | Total course interactions during the course |
| `early_click` | Interactions during the first 14 days |
| `early_active_days` | Number of active learning days early in course |
| `first_activity_day` | Day when student first interacted with course |
| `pre_course_engaged` | Whether student interacted before course start |

These features capture **timing, intensity, and consistency of engagement**.

---

# ⚙️ System Architecture

```
User Interface (Streamlit)
        ↓
predict_and_recommend()
        ↓
Input Validation
        ↓
Feature Builder
        ↓
Machine Learning Model
        ↓
Recommendation Engine
        ↓
Explainable AI
        ↓
Results Display
```

---

# 🏗 Project Structure

```
student-engagement-risk-prediction-recommendation-system
│
├── app.py
│
├── core
│   ├── feature_builder.py
│   ├── predictor.py
│   └── recommender.py
│
├── utils
│   ├── model_loader.py
│   ├── validators.py
│   └── path_utils.py
│
├── models
│   └── artefacts
│       └── finalized_model.joblib
│
├── config
│   └── config.yaml
│
└── README.md
```

---

# 🤖 Machine Learning Model

Model used:

```
Decision Tree Classifier
```

Reason for choosing:

- Interpretable
- Easy to explain decisions
- Suitable for explainable AI systems

The system predicts:

```
Risk Probability
```

Which is converted into:

| Risk Level | Probability |
|------|------|
| Low | < 0.30 |
| Medium | 0.30 – 0.60 |
| High | > 0.60 |

---

# 🔍 Explainable AI

The system also explains **why a prediction was made** by analyzing the path taken inside the decision tree.

Example explanation:

```
Early Click <= 71
Total Click <= 377
First Activity Day > 0
```

This helps instructors understand **which behavioral patterns triggered the risk prediction**.

---

# 📢 Recommendation System

Instead of only predicting risk, the system generates **actionable recommendations**.

Example output:

### Observations

- No engagement in early course period
- Low early interaction with course content
- Late course start compared to peers

### Recommended Actions

- Watch introductory videos
- Follow a structured 7-day recovery plan
- Participate in forum discussions
- Schedule academic mentoring session

---

# 🖥 Streamlit Application

The Streamlit interface allows users to interactively simulate student engagement behavior.

Users can input:

- Total course interactions
- Early course engagement
- Early active learning days
- First activity timing
- Pre-course engagement

The system then returns:

- Risk level
- Risk probability
- Observations
- Recommended actions
- Model explanation

---

# ☁ Deployment

The application is deployed using:

```
Streamlit Cloud
```

Live URL:

https://student-engagement-risk-prediction-recommendation-system.streamlit.app

---

# 🛠 Tech Stack

**Programming**

- Python

**Libraries**

- pandas
- scikit-learn
- joblib
- streamlit
- yaml

**ML Concepts**

- Feature Engineering
- Behavioral Signal Analysis
- Decision Tree Modeling
- Explainable AI
- Recommendation Systems

---

# 📚 Learning Outcomes

This project demonstrates:

- Building ML pipelines
- Feature engineering for behavioral data
- Designing explainable ML systems
- Creating recommendation systems
- Modular ML project architecture
- Deploying ML applications

---

# 📌 Future Improvements

Possible extensions include:

- Using more advanced ML models
- Adding time-series engagement analysis
- Integrating LMS data sources
- Personalized learning path generation
- Instructor dashboard for monitoring student risk

---

# 👨‍💻 Author

**Musharraf Bubare**

GitHub  
https://github.com/Musharraf-Bubere

---

# ⭐ If you found this project useful

Please consider **starring the repository**.
