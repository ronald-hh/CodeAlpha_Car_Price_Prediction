# Car Price Prediction

This project uses machine learning to predict the selling price of a used car based on its features.

The notebook builds and compares several regression models to estimate a car's resale value using information such as its age, mileage, fuel type, transmission, and current market price.

---

## Dataset

The project uses the **Car Price Prediction** dataset (`car_data.csv`).

The dataset contains information such as:
- Car Name
- Year
- Selling Price (Target)
- Present Price
- Kilometers Driven
- Fuel Type
- Seller Type
- Transmission
- Number of Previous Owners

The notebook creates a new feature called **Car_Age** from the `Year` column and removes the `Car_Name` column since it is not useful for prediction.

---

## What the Notebook Does

The notebook follows these steps:

1. Import the required Python libraries.
2. Load and inspect the dataset.
3. Clean and prepare the data.
4. Perform exploratory data analysis (EDA).
5. Create new features and encode categorical variables.
6. Split and scale the data.
7. Train multiple regression models.
8. Compare model performance.
9. Evaluate the best-performing model.
10. Display feature importance.
11. Predict the selling price of a new car using custom inputs.

---

## Models Used

The notebook compares the following regression models:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor

---

## Libraries Used

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## Requirements

Install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

---

## How to Run

1. Download or clone this project.
2. Place `car_data.csv` in the same folder as `Car_Price_Prediction.ipynb`.
3. Open the notebook.

```bash
jupyter notebook Car_Price_Prediction.ipynb
```

4. Run all cells from top to bottom.

---

## Make Predictions

At the end of the notebook, you can predict the selling price of a car by entering its details:

```python
predict_price(
    present_price,
    driven_kms,
    car_age,
    owner,
    fuel_type,
    selling_type,
    transmission
)
```

Example:

```python
predict_price(
    present_price=6.5,
    driven_kms=45000,
    car_age=5,
    owner=0,
    fuel_type="Petrol",
    selling_type="Dealer",
    transmission="Manual"
)
```

---

## Model Evaluation

The models are evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score
- Residual Analysis
- 5-Fold Cross-Validation

These metrics help determine how accurately the models predict car prices.

---

## Results

The notebook compares six regression models and selects the best-performing one based on evaluation metrics.

The analysis also shows that:

- Present Price is the most important feature for predicting resale value.
- Older cars generally have lower selling prices.
- Higher mileage usually reduces resale value.
- Fuel type, transmission, and seller type also influence the selling price.

Cross-validation is included to provide a more reliable estimate of how well the model performs on unseen data.

---

## Workflow

```text
Load Data
    ↓
Clean Data
    ↓
Explore Data
    ↓
Feature Engineering
    ↓
Prepare Data
    ↓
Train Models
    ↓
Compare Results
    ↓
Evaluate Best Model
    ↓
Predict Car Prices
```

---

## Project Goal

The goal of this project is to demonstrate a complete machine learning regression workflow using real-world car sales data. It covers data preprocessing, exploratory data analysis, feature engineering, model training, evaluation, and prediction of used car prices.
