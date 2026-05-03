# Higher Education AI Support Ticket Router

An AI-powered system that classifies student support tickets into appropriate university departments using Natural Language Processing (NLP).

---

## 🚀 Features

- Classifies student support requests into:
  - Admissions
  - Course Registration
  - Financial Aid
  - Academic Advising
  - Graduation
  - Technical Support
- Displays prediction confidence
- Provides top-3 category predictions
- Includes routing logic (auto-route / review / escalate)
- Interactive web app built with Streamlit

---

## 🧠 Model Comparison

| Model | Accuracy |
|------|--------|
| Linear SVM | 70.97% |
| Logistic Regression | 67.74% |
| Naive Bayes | 64.52% |
| Random Forest | 58.06% |

Although **Linear SVM** achieved the highest accuracy, **Logistic Regression** was selected for deployment because it supports probability outputs (`predict_proba()`), enabling confidence-based routing decisions.

---

## ⚙️ How It Works

1. Text input is transformed using **TF-IDF vectorization**
2. A machine learning model classifies the request
3. The system:
   - predicts the category
   - calculates confidence
   - applies routing rules:
     - ≥ 70% → Auto-route
     - 40–70% → Review queue
     - < 40% → Escalate

---

## 📁 Project Structure

