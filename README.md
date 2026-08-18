# 🏠 House Price Prediction

## 📌 Project Overview

This project predicts house prices using **Machine Learning and Linear Regression**.

The dataset contains information about houses such as area, number of bedrooms, bathrooms, stories, parking, and other house-related features. The model learns the relationship between these features and the house price, then predicts prices for unseen data.

## 📊 Dataset

* **Rows:** 545
* **Original Columns:** 13
* **Target Variable:** `price`
* **Dataset File:** `Housing.csv`

### Main Features

* `area`
* `bedrooms`
* `bathrooms`
* `stories`
* `parking`
* `mainroad`
* `guestroom`
* `basement`
* `hotwaterheating`
* `airconditioning`
* `prefarea`
* `furnishingstatus`

## 🔧 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Checked the dataset structure and data types.
3. Checked for missing values.
4. Checked for duplicate rows.
5. Converted binary `yes/no` values into `1/0`.
6. Identified the remaining categorical feature.
7. Applied **One-Hot Encoding** to `furnishingstatus`.
8. Combined the processed numerical and encoded features.

## 🤖 Machine Learning Model

The project uses:

**Linear Regression**

The dataset was divided into:

* **70% Training Data**
* **30% Testing Data**

The model was trained using the training data and evaluated on the unseen test data.

## 📈 Model Evaluation

The model was evaluated using:

* **MAE (Mean Absolute Error):** ~920,393
* **MSE (Mean Squared Error):** ~1.523 × 10¹²
* **RMSE (Root Mean Squared Error):** ~1,234,107
* **R² Score:** ~0.646

The R² score indicates that the Linear Regression model explains approximately **64.6% of the variation** in house prices on the test data.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook

## 📁 Project Structure

```text
House Price Predictor/
│
├── Housing.csv
├── Housing_Price_Prediction.ipynb
└── README.md
```

## 🚀 How to Run

1. Clone or download this repository.
2. Open `Housing_Price_Prediction.ipynb` in Jupyter Notebook or VS Code.
3. Make sure `Housing.csv` is in the same project folder.
4. Run the notebook cells in order.

## 🎯 Project Goal

The main goal of this project is to understand the complete Machine Learning workflow:

**Data → Preprocessing → Encoding → Train/Test Split → Model Training → Prediction → Evaluation**

## 📌 Future Improvements

The model's performance can potentially be improved by:

* Handling outliers
* Performing feature analysis and selection
* Trying feature scaling where appropriate
* Comparing Linear Regression with Ridge and Lasso Regression
* Testing other regression models
* Hyperparameter tuning and cross-validation



# 📚 Student Performance Prediction

## 📌 Project Overview

This project uses **Machine Learning and Linear Regression** to predict a student's `exam_score` based on different student habits and academic factors.

The project follows a complete Machine Learning workflow:

**Data Loading → Data Cleaning → Encoding → Train/Test Split → Model Training → Prediction → Evaluation**

## 📊 Dataset

The project uses the **Student Habits & Performance** dataset.

- **Rows:** 1,000 students
- **Original Columns:** 16
- **Target Variable:** `exam_score`
- **Dataset File:** `student_habits_performance.csv`

### Main Features

The model uses features such as:

- `age`
- `gender`
- `study_hours_per_day`
- `social_media_hours`
- `netflix_hours`
- `part_time_job`
- `attendance_percentage`
- `sleep_hours`
- `diet_quality`
- `exercise_frequency`
- `parental_education_level`
- `internet_quality`
- `mental_health_rating`
- `extracurricular_participation`

The target variable is:

- `exam_score`

## 🔧 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Explored the dataset using `head()`, `shape()`, and `info()`.
3. Checked for missing values.
4. Filled missing values in `parental_education_level` using its most frequent category (mode).
5. Checked for duplicate rows.
6. Removed `student_id` because it is only an identifier and does not provide useful predictive information.
7. Converted `gender` into numerical values.
8. Identified the remaining categorical columns.
9. Applied **One-Hot Encoding** to the remaining categorical features.
10. Combined the numeric and encoded features into the final dataset.

## 🤖 Machine Learning Model

The project uses:

**Linear Regression**

The dataset was divided into:

- **70% Training Data**
- **30% Testing Data**

The model was trained using the training data and evaluated on unseen test data.

## 📈 Model Evaluation

The model was evaluated using:

| Metric | Result |
|---|---:|
| MAE | ~4.27 marks |
| MSE | ~28.61 |
| RMSE | ~5.35 marks |
| R² Score | ~0.897 |

### What do these results mean?

- **MAE ≈ 4.27:** On average, predictions differ from actual exam scores by about 4.27 marks.
- **RMSE ≈ 5.35:** Larger prediction errors have a stronger effect on this metric.
- **R² ≈ 0.897:** The model explains approximately **89.7% of the variation** in exam scores on the test set.

Overall, the Linear Regression model performs well on this dataset.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook

## 📁 Project Structure

```text
Student Performance Predictor/
│
├── student_habits_performance.csv
├── main (1).ipynb
└── README.md
