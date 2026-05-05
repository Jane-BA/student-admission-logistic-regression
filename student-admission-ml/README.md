# 🎓 Student Admission Prediction (Logistic Regression + Power BI)

## 📌 Overview

This project builds a classification model to predict whether a student is admitted based on two exam scores.

The focus is not only on modeling, but on **feature engineering, model interpretation, and data visualization using Power BI**.

---

## 🧠 Problem Statement

**Given:** Exam 1 score & Exam 2 score

**Predict:** Admission status (0 = Not Admitted, 1 = Admitted)

---

## ⚙️ Approach

## 1. Baseline Model

**Logistic Regression using**: Exam 1 & Exam 2

📉 Result:

◈ Accuracy: **0.80**\
◈ Limitation: linear decision boundary

### 2. Feature Engineering

New features were created to capture non-linear relationships:

**Average** → overall performance\
**Synergy (Exam1 * Exam2)** → interaction between variables\
**Difference** → consistency between exams\
**Ratio** → relative performance\
**Max / Min** → best and worst scores\
**Squared features** → allow curved boundaries\
**Distance to Ideal (100,100)** → key feature

🚀 The *distance to ideal* captures overall performance in a single variable.

### 3. Advanced Model

Using:

* Exam1²
* Exam2²
* Distance to Ideal

📈 Result:

* Accuracy: **1.00**

### 4. Model Insights

▷ The model learns a **non-linear decision boundary**\
▷ Admission is driven by:\
    ⊳ overall performance (distance)\
    ⊳ consistency (minimum score)\
▷ Logistic regression produces **probabilities (sigmoid output)**, not just classes

---

## 📊 Power BI Dashboard

The project includes an interactive dashboard built in Power BI:

### Key elements:

✔️ KPI: total students and admission rate\
✔️ Scatter plot: Exam 1 vs Exam 2 colored by probability\
✔️ Relationship: distance vs probability\
✔️ Filters for exploration

📌 Insight:

> Students closer to the ideal point (100,100) have significantly higher admission probability.

---

## 📁 Project Structure

```
student-admission-logistic-regression/
│
├── data/
│   └── resultados_modelo.csv
│
├── notebook/
│   └── modelo.ipynb
│
├── powerbi/
│   └── dashboard.pbix
│
├── images/
│   └── dashboard.png
│
├── README.md
└── requirements.txt
```

---

## 🚀 How to Run

```bash
git clone https://github.com/tu_usuario/student-admission-logistic-regression.git
cd student-admission-logistic-regression
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook
```

---

## 🧠 Key Takeaways

✔️ Feature engineering can outperform complex models\
✔️ Logistic regression can model non-linear behavior with proper transformations\
✔️ Visualization (Power BI) is critical to communicate insights\
✔️ Probabilities provide more information than binary predictions

---

## ⚠️ Limitations

‼ Small dataset → possible overfitting\
‼ High accuracy may not generalize\
‼ Results depend heavily on engineered features

---

## 🛠️ Technologies

» Python\
» Pandas\
» NumPy\
» Scikit-learn\
» Matplotlib\
» Power BI

---

## 💡 Author

This project focuses on bridging:
**Machine Learning + Business Visualization**

---
