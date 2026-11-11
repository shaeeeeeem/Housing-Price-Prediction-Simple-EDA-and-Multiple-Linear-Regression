# Housing Price Prediction — Exploratory Data Analysis & Multiple Linear Regression

## Overview
This project predicts residential house prices using continuous and categorical features from the `Housing.csv` dataset. Because the target variable (`price`) is a continuous numeric value, this problem is solved using **Multiple Linear Regression** rather than classification algorithms like Logistic Regression.

---

## Project Objectives
- Perform Exploratory Data Analysis (EDA) to understand feature distributions, correlations, and relationships with house prices.
- Preprocess data by handling categorical variables (encoding binary and multi-class categories) and feature scaling.
- Train and evaluate a Multiple Linear Regression model to identify key price drivers and assess predictive performance.

---

## Dataset Description
The dataset contains records of housing properties with features covering size, room counts, and amenities:

| Feature | Type | Description |
| :--- | :--- | :--- |
| `price` | Numeric | House sale price (target variable) |
| `area` | Numeric | Total surface area of the house in square feet |
| `bedrooms` | Numeric | Total number of bedrooms |
| `bathrooms` | Numeric | Total number of bathrooms |
| `stories` | Numeric | Number of stories/floors |
| `mainroad` | Categorical | Proximity to the main road (`yes` / `no`) |
| `guestroom` | Categorical | Presence of a guest room (`yes` / `no`) |
| `basement` | Categorical | Presence of a basement (`yes` / `no`) |
| `hotwaterheating` | Categorical | Presence of hot water heating (`yes` / `no`) |
| `airconditioning` | Categorical | Presence of central air conditioning (`yes` / `no`) |
| `parking` | Numeric | Number of parking spots available |
| `prefarea` | Categorical | Located in a preferred neighborhood (`yes` / `no`) |
| `furnishingstatus` | Categorical | Furnishing condition (`furnished`, `semi-furnished`, `unfurnished`) |

---

## Tech Stack & Libraries
- **Language:** Python
- **Data Manipulation:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Machine Learning:** `scikit-learn` (or `statsmodels`)

---

## Workflow & Steps

1. **Environment Setup & Data Loading:**
   - Load `Housing.csv` and inspect structure, summary statistics, and missing values.

2. **Exploratory Data Analysis (EDA):**
   - Visualize target distribution (`price`) for skewness.
   - Plot scatter plots and pair plots against `area` and continuous predictors.
   - Use box plots to analyze categorical amenities against price.
   - Generate a correlation heatmap to detect collinearity among numeric variables.

3. **Data Preprocessing:**
   - Map binary categorical variables (`yes`/`no`) to `1`/`0`.
   - Apply one-hot encoding (or dummy variables) with `drop_first=True` for `furnishingstatus`.
   - Split data into training and test sets (e.g., 70/30 or 80/20 split).
   - Apply feature scaling (e.g., `MinMaxScaler` or `StandardScaler`) where appropriate.

4. **Model Training & Evaluation:**
   - Fit a Multiple Linear Regression model.
   - Evaluate model fit using:
     - **$R^2$ Score** (Coefficient of Determination)
     - **Mean Absolute Error (MAE)**
     - **Root Mean Squared Error (RMSE)**
   - Perform residual analysis to verify assumptions of linearity, homoscedasticity, and normal distribution of residuals.

---

## Getting Started

### Prerequisites
Install the required dependencies:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
