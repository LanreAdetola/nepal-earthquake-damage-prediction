# 🌍 Nepal Earthquake Damage Prediction (DrivenData Challenge)

This project was developed as part of a data science assignment focused on **binary classification** using real-world humanitarian data.  
The goal is to predict building damage levels after the 2015 Nepal earthquake.

---

## 🎯 Project Overview

This project adapts the original [DrivenData Nepal Earthquake Challenge](https://www.drivendata.org/competitions/57/nepal-earthquake/) into a **binary classification task**:

- **Target Variable**: `damage_grade`
- **Classes:**
  - **Low Damage** → Grades 1 & 2
  - **Severe Damage** → Grade 3

The dataset includes information about the **building structures**, **materials**, and **geo-locations**, which were used to predict post-disaster damage levels.

---

## 📘 Notebook Overview

The main notebook [`solution.ipynb`](notebooks/solution.ipynb) contains the following sections:

1. **Data Exploration**  
   - Overview of dataset shape, missing values, and feature distributions.

2. **Data Cleaning**  
   - Handled missing or inconsistent values.  
   - Converted categorical variables to numeric (label/one-hot encoding).

3. **Feature Engineering**  
   - Combined or transformed features to improve model signal.

4. **Model Training & Validation**  
   - Used cross-validation and hyperparameter tuning.  
   - Tested different algorithms (e.g., Logistic Regression, Random Forest, XGBoost).

5. **Evaluation Metrics**  
   - ROC Curve (AUC)
   - Precision-Recall Curve
   - Confusion Matrix

6. **Final Model Evaluation**  
   - Model retrained on full training set and evaluated on test data.

---

## ⚙️ Installation & Usage

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/nepal-earthquake-ml.git
cd nepal-earthquake-ml
```

### 2️⃣ Create a Virtual Environment
```bash
python -m venv venv
source venv/bin/activate    # macOS/Linux
venv\Scripts\activate       # Windows
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 4️⃣ Run the Notebook
```bash
jupyter notebook notebooks/solution.ipynb
```

---

## 🧩 Dependencies

Add these to your `requirements.txt`:

```
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
jupyter
```

---


## 📈 Results Summary

| Model | Accuracy | Precision | Recall | F1-Score |
|--------|-----------|------------|----------|-----------|
| **Logistic Regression** | 0.672 | 0.546 | 0.114 | 0.188 |
| **Random Forest** | **0.748** | **0.661** | **0.505** | **0.573** |

---

### 🧠 Insights

- **Random Forest** outperformed Logistic Regression across all metrics, showing stronger capability to capture non-linear relationships.  
- Logistic Regression’s low recall (0.114) suggests underfitting — it struggles to detect buildings with severe damage.  
- Random Forest achieved a better **balance between recall and precision**, indicating more reliable predictions for both classes.  
- The next improvement step could involve **hyperparameter tuning**, **class balancing (SMOTE)**, or trying **XGBoost** to push recall higher without losing precision.
## 🚀 Future Improvements

- Add deep learning baseline (e.g., TensorFlow or PyTorch).
- Include geospatial analysis of damage distribution.
- Automate preprocessing with pipelines.
- Deploy as an API using FastAPI or Flask.

---

## 🧑‍💻 Author

**Lanre Adetola**  
BSc Information Management – Data Science, Protection & Security  
[LinkedIn](https://www.linkedin.com/in/lanre-adetola0/) • [GitHub](https://github.com/LanreAdetola)

---

> 📚 *Originally submitted for a university assignment (score: 17/20). Continues to evolve as a real-world machine learning case study.*
