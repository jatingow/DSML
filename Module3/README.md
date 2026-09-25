# Module 3 – Machine Learning Fundamentals: Regression & Classification

Welcome to **Module 3**!

This module provides hands-on introductions to supervised machine learning, comparing continuous regression tasks with discrete binary classification tasks using Scikit-Learn.

---

## 📚 Contents

### 💻 Project Notebooks (`project-notebooks/`)
Contains Google Colab and Jupyter Notebook files covering practical machine learning workflows:

1. **[`Linear_Regression_Student_Marks.ipynb`](file:///d:/DSML/ML-DataScience-Training/Module3/project-notebooks/Linear_Regression_Student_Marks.ipynb)**
   - **Task**: Simple Linear Regression
   - **Scenario**: Modeling the relationship between study hours and student exam marks.
   - **Highlights**: Feature-target separation, fitting a `LinearRegression` model, visualizing the line of best fit, and predicting continuous marks.

2. **[`Logistic_Regression_Student_Pass_Fail.ipynb`](file:///d:/DSML/ML-DataScience-Training/Module3/project-notebooks/Logistic_Regression_Student_Pass_Fail.ipynb)**
   - **Task**: Binary Logistic Regression
   - **Scenario**: Predicting whether a student passes or fails based on study hours.
   - **Highlights**: Fitting a `LogisticRegression` classifier, estimating outcome probability (`predict_proba`), and decision threshold classification (`predict`).

---

## 🔍 Key Concepts Covered

- **Supervised Learning Fundamentals**:
  - Independent variables / Features ($X$) vs. Dependent variable / Target ($y$).
  - Preparing 2D feature matrices (`df[["Hours"]]`) for Scikit-Learn.
- **Regression vs. Classification**:
  - Predicting continuous values vs. categorical classes and event probabilities.
- **Scikit-Learn Standard API Pattern**:
  - Model Initialization $\rightarrow$ Model Fitting (`.fit(X, y)`) $\rightarrow$ Inference (`.predict(X_new)` / `.predict_proba(X_new)`).
- **Data Visualization**:
  - Visualizing relationships and model predictions using Matplotlib scatter and line plots.

---

## 🚀 How to Run the Notebooks

1. Navigate to the [`project-notebooks`](file:///d:/DSML/ML-DataScience-Training/Module3/project-notebooks) directory.
2. Select either notebook (`.ipynb`).
3. Run locally via Jupyter Notebook / VS Code, or upload directly to [Google Colab](https://colab.research.google.com/).
4. Run the cells step-by-step to observe model training and predictions.
