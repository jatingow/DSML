# Module 3 – Supervised Machine Learning: Regression & Classification

Welcome to **Module 3** of the Data Science & Machine Learning training!

This module introduces fundamental **Supervised Machine Learning** algorithms using Python, Pandas, Matplotlib, and Scikit-Learn (`sklearn`). It focuses on two foundational modeling techniques:
1. **Linear Regression** (Predicting continuous numeric values)
2. **Logistic Regression** (Predicting binary categorical outcomes & probabilities)

---

## 📂 Folder Structure

```text
Module3/
├── README.md
└── project-notebooks/
    ├── README.md
    ├── Linear_Regression_Student_Marks.ipynb
    └── Logistic_Regression_Student_Pass_Fail.ipynb
```

---

## 📓 Notebook Walkthroughs

### 1. `Linear_Regression_Student_Marks.ipynb`
* **Machine Learning Task**: Simple Linear Regression (Continuous Target)
* **Goal**: Predict a student's examination marks based on the number of hours they studied.

#### Workflow:
1. **Import Libraries**:
   - `pandas` for tabular data management
   - `matplotlib.pyplot` for data visualization
   - `sklearn.linear_model.LinearRegression` for model training
2. **Dataset Creation**:
   - Feature ($X$): `Hours` $[1, 2, 3, \dots, 10]$
   - Target ($y$): `Marks` $[35, 40, 48, \dots, 90]$
3. **Feature-Target Split**:
   - $X = \text{df}[[\text{"Hours"}]]$ (2D array/DataFrame as required by Scikit-Learn)
   - $y = \text{df}[\text{"Marks"}]$ (1D series target)
4. **Model Training**:
   - Initialized `LinearRegression()`
   - Fitted the model using `model.fit(X, y)` to find the optimal slope ($m$) and intercept ($c$) for $y = mx + c$.
5. **Visualization**:
   - Plotted data points with `plt.scatter(X, y)`
   - Plotted the best-fit regression line using `plt.plot(X, model.predict(X))`
6. **Inference**:
   - Evaluated a test case with 7 study hours (`model.predict([[7]])`), producing the predicted exam score.

---

### 2. `Logistic_Regression_Student_Pass_Fail.ipynb`
* **Machine Learning Task**: Binary Classification (Categorical Target / Probability)
* **Goal**: Predict whether a student will Pass ($1$) or Fail ($0$) based on study hours, along with the confidence probability.

#### Workflow:
1. **Import Libraries**:
   - `pandas`, `matplotlib.pyplot`, and `sklearn.linear_model.LogisticRegression`
2. **Dataset Creation**:
   - Feature ($X$): `Hours` $[1, 2, 3, \dots, 10]$
   - Target ($y$): `Pass` $[0, 0, 0, 1, 1, 1, 1, 1, 1, 1]$ ($0 = \text{Fail}$, $1 = \text{Pass}$)
3. **Feature-Target Split**:
   - $X = \text{df}[[\text{"Hours"}]]$
   - $y = \text{df}[\text{"Pass"}]$
4. **Model Training**:
   - Initialized `LogisticRegression()`
   - Fitted the model with `model.fit(X, y)` using the sigmoid (logistic) function to map inputs between 0 and 1.
5. **Visualization**:
   - Plotted the binary distribution of outcomes across study hours with `plt.scatter(X, y)`.
6. **Inference & Probability Estimation**:
   - Evaluated a student studying 4.5 hours (`hours = [[4.5]]`).
   - Calculated probability of passing using `model.predict_proba(hours)[0][1]`.
   - Determined the final class classification ($0$ or $1$) using `model.predict(hours)[0]`.

---

## ⚖️ Linear Regression vs. Logistic Regression

| Feature | Linear Regression | Logistic Regression |
| :--- | :--- | :--- |
| **Problem Type** | Regression | Classification |
| **Output Type** | Continuous numerical value (e.g., Marks: `70.5`) | Discrete class / Probability (e.g., Pass: `1`, Fail: `0`) |
| **Core Function** | Linear equation: $y = mx + c$ | Sigmoid function: $P(Y=1) = \frac{1}{1 + e^{-z}}$ |
| **Output Range** | $(-\infty, +\infty)$ | $[0, 1]$ |
| **Key Scikit-Learn API** | `model.predict(X)` | `model.predict(X)`, `model.predict_proba(X)` |

---

## 🛠️ Requirements & Installation

To run these notebooks locally or in an environment like Google Colab, make sure you have the following Python packages installed:

```bash
pip install pandas matplotlib scikit-learn jupyter
```

---

## 🚀 How to Run the Notebooks

1. **Google Colab**:
   - Open [Google Colab](https://colab.research.google.com/).
   - Click **File** > **Upload notebook**.
   - Select either `Linear_Regression_Student_Marks.ipynb` or `Logistic_Regression_Student_Pass_Fail.ipynb`.
   - Connect to the runtime and execute cells sequentially (`Shift + Enter`).

2. **Local Jupyter Notebook / VS Code**:
   - Open your terminal in this repository.
   - Launch Jupyter:
     ```bash
     jupyter notebook
     ```
   - Navigate to `Module3/project-notebooks/` and open either notebook.
