# 🐚 Abalone Age Prediction

## 📌 Project Overview

This project uses the Abalone dataset to predict the **age of abalones** based on their physical measurements. Since counting rings manually is difficult, machine learning is used to estimate the number of rings, which determines age.

---

## 📂 Dataset

The dataset is sourced from the UCI Machine Learning Repository and contains information about abalones such as size and weight measurements.

### Features:

* Sex (M, F, I)
* Length
* Diameter
* Height
* Whole_weight
* Shucked_weight
* Viscera_weight
* Shell_weight

### Target:

* Rings (used to calculate age)

👉 Age ≈ Rings + 1.5 years

---

## ⚙️ Technologies Used

* Python 🐍
* Pandas
* NumPy
* Scikit-learn

---

## 🔀 Train-Test Split

The dataset is divided into:

* **Training Data (80%)** – used to train the model
* **Testing Data (20%)** – used to evaluate performance

```python
from sklearn.model_selection import train_test_split

X = data.drop("Rings", axis=1)
y = data["Rings"]

X = pd.get_dummies(X, columns=["Sex"])

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```

---

## 🤖 Model Used

A **Random Forest Regressor** is used for predicting the number of rings.

```python
from sklearn.ensemble import RandomForestRegressor

model = RandomForestRegressor()
model.fit(X_train, y_train)
```

---

## 📊 Evaluation

The model performance can be evaluated using metrics like:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* R² Score

---

## 🚀 How to Run

1. Clone the repository:

```
git clone https://github.com/your-username/abalone-age-prediction.git
```

2. Install dependencies:

```
pip install -r requirements.txt
```

3. Run the project:

```
python src/model.py
```

---

## 📌 Conclusion

This project demonstrates how machine learning can be used to predict the age of abalones using physical characteristics. It covers data preprocessing, train-test splitting, and regression modeling.

---

## 📎 Author

Shravani Waikar

