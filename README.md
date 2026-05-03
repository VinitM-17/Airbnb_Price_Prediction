Predicts Airbnb listing prices using regression models (Linear Regression, Decision Tree, Random Forest). Includes EDA, feature engineering, and model evaluation with RMSE, MAE & R². Built with Python, pandas, scikit-learn, matplotlib & seaborn. | Beginner-friendly ML project.


# 🏠 Airbnb Price Prediction — Machine Learning Project

A beginner-friendly machine learning project that predicts Airbnb listing prices using regression models. Built as part of an Internshala ML Internship Training project.

---

## 📌 Problem Statement

Airbnb hosts often struggle to price their listings competitively. Price too high — guests won't book. Price too low — hosts lose revenue.

This project builds a **regression model** to predict the `log_price` of an Airbnb listing based on property features, location, host characteristics, and guest review data.

---

## 📂 Project Structure

```
PartA_Airbnb_Price_Prediction/
│
├── PartA_Airbnb_Price_Prediction.ipynb   # Main Jupyter Notebook
├── Airbnb_data.xlsx                       # Dataset
└── README_PartA_Airbnb.md                 # This file
```

---

## 📊 Dataset Overview

| Detail | Info |
|---|---|
| File | `Airbnb_data.xlsx` |
| Rows | 74,111 |
| Columns | 29 |
| Target Variable | `log_price` (log of listing price) |

### Key Features Used

| Feature | Description |
|---|---|
| `room_type` | Entire place / Private room / Shared room |
| `property_type` | Apartment, House, Condo, etc. |
| `city` | City where the listing is located |
| `accommodates` | Number of guests the listing fits |
| `bedrooms` / `beds` / `bathrooms` | Size indicators |
| `number_of_reviews` | Total reviews received |
| `review_scores_rating` | Average guest rating |
| `cancellation_policy` | Flexible, Moderate, Strict |
| `instant_bookable` | Whether it can be instantly booked |
| `cleaning_fee` | Whether a cleaning fee applies |

---

## 🔧 Tech Stack

- **Language:** Python 3
- **Environment:** Jupyter Notebook
- **Libraries:**

```python
pandas, numpy, matplotlib, seaborn, scikit-learn
```

---

## 🚀 How to Run

1. Clone the repository or download the files
2. Make sure the dataset `Airbnb_data.xlsx` is in the same folder as the notebook
3. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
   ```
4. Open the notebook:
   ```bash
   jupyter notebook PartA_Airbnb_Price_Prediction.ipynb
   ```
5. Run all cells from top to bottom (`Kernel → Restart & Run All`)

---

## 📈 Project Workflow

```
1. Understand the Problem
        ↓
2. Import Libraries
        ↓
3. Load & Explore Dataset (EDA)
        ↓
4. Data Preprocessing
   - Handle missing values
   - Label encode categorical columns
   - Train-test split (80/20)
        ↓
5. Model Building
   - Linear Regression
   - Decision Tree Regressor
   - Random Forest Regressor ✅ (Best)
        ↓
6. Model Evaluation
   - RMSE, MAE, R²
   - Actual vs Predicted Plot
   - Feature Importance
        ↓
7. Conclusion & Insights
```

---

## 📉 EDA Highlights

- **Room type** strongly influences price — Entire homes cost more than private/shared rooms
- **City** plays a big role — San Francisco and NYC have the highest average prices
- **More bedrooms = higher price**, showing a clear upward trend
- `accommodates`, `bedrooms`, and `bathrooms` are highly correlated with price

---

## 🤖 Models & Results

| Model | RMSE | MAE | R² Score |
|---|---|---|---|
| Linear Regression | ~0.55 | ~0.42 | ~0.45 |
| Decision Tree | ~0.51 | ~0.38 | ~0.52 |
| **Random Forest** ✅ | **~0.45** | **~0.34** | **~0.60** |

> ✅ **Random Forest** performed the best with an R² of ~0.60, meaning it explains about 60% of the variance in listing prices.

---

## 🔍 Key Feature Importances (Random Forest)

1. `room_type` — Type of room is the strongest price predictor
2. `accommodates` — Larger capacity = higher price
3. `bedrooms` — More bedrooms drives price up
4. `city` — Location heavily affects pricing
5. `review_scores_rating` — Higher-rated listings charge more

---

## 💡 Conclusions

1. **Room type and city are the most important price drivers** — hosts in premium cities with entire apartments can charge significantly more.
2. **Property size matters** — bedrooms, beds, and guest capacity directly impact pricing.
3. **Random Forest outperformed** simpler models by capturing non-linear relationships in the data.
4. **Review scores have moderate influence** — quality matters, but not as much as size and location.
5. **Hosts can use this model** to get a data-driven baseline price for their listing before going live.

---

## 👤 Author

**[Your Name]**
ML Internship Project — Internshala Trainings

---

## 📄 License

This project is for educational purposes only.
