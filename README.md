# Employee Salary Prediction System

## Project Description

Employee Salary Prediction System built using Python and Machine Learning. The project generates a synthetic employee dataset, performs data preprocessing and exploratory data analysis, and trains a regression model to predict salaries based on age, education, experience, skills, certifications, job role, and company type with high accuracy.

---

## Project Overview

The Employee Salary Prediction System is a Machine Learning project that predicts employee salaries using various demographic and professional factors. The project follows a complete data science workflow including dataset generation, preprocessing, exploratory data analysis (EDA), model training, evaluation, and salary prediction.

The objective is to analyze how factors such as education, experience, skills, certifications, and job roles influence employee salaries and build a predictive model that can estimate salary accurately.

---

## Dataset Generation / Loading Process

### Dataset Generation

A synthetic dataset containing 2,500 employee records was generated using NumPy and Pandas.

### Features Included

* Age
* Education Level
* Years of Experience
* Skills Score
* Number of Certifications
* Job Role
* Company Type
* Salary (Target Variable)

### Salary Calculation Logic

Salary values were generated based on:

* Base salary
* Experience bonus
* Skills score contribution
* Certification bonus
* Education bonus
* Job role bonus
* Company type bonus
* Random salary variation for realism

### Data Quality Simulation

To mimic real-world datasets:

* 2% missing values were introduced in Education.
* 2% missing values were introduced in SkillsScore.
* 20 duplicate records were added intentionally.

### Dataset Statistics

| Description             | Count |
| ----------------------- | ----- |
| Initial Records         | 2520  |
| Duplicate Records Added | 20    |
| Final Clean Records     | 2500  |
| Features                | 8     |

---

## Libraries Used

| Library                 | Purpose                                                    |
| ----------------------- | ---------------------------------------------------------- |
| Pandas                  | Data loading, cleaning, preprocessing, and manipulation    |
| NumPy                   | Synthetic data generation and numerical computations       |
| Matplotlib              | Data visualization and plotting                            |
| Seaborn                 | Statistical visualization and correlation analysis         |
| Scikit-learn            | Machine learning model building and evaluation             |
| LabelEncoder            | Encoding categorical variables into numerical values       |
| StandardScaler          | Feature scaling and normalization                          |
| Train-Test Split        | Splitting dataset into training and testing sets           |
| Random Forest Regressor | Salary prediction model                                    |
| Evaluation Metrics      | Performance measurement using MAE, MSE, RMSE, and R² Score |

### Import Statements

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.preprocessing import LabelEncoder, StandardScaler
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score
```

---

## Data Preprocessing

The preprocessing pipeline includes:

### Handling Missing Values

* Missing Education values filled using Mode.
* Missing SkillsScore values filled using Mean.

### Removing Duplicate Records

* Duplicate rows identified and removed.

### Data Validation

* Age restricted between 18 and 65.
* Experience values validated.
* Salary values ensured to be positive.

### Encoding Categorical Features

The following columns were encoded:

* Education
* JobRole
* CompanyType

### Feature Scaling

The following numerical columns were standardized:

* Age
* Experience
* SkillsScore
* Certifications

---

## Exploratory Data Analysis (EDA)

Several visualizations were created to understand employee salary trends.

### Analysis Performed

* Salary Distribution
* Experience vs Salary
* Education vs Salary
* Job Role vs Salary
* Company Type vs Salary
* Correlation Heatmap
* Feature Distribution Analysis

---

## Machine Learning Model

### Model Used

Random Forest Regressor

### Training Process

1. Dataset prepared after preprocessing.
2. Features and target variable separated.
3. Dataset split into:

   * 80% Training Data
   * 20% Testing Data
4. Model trained using Random Forest Regression.
5. Predictions generated on test data.

---

## Steps to Run the Project

### Step 1: Clone the Repository

```bash
git clone <repository-url>
```

### Step 2: Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Step 3: Run the Project

```bash
python employee_salary_prediction_model.py
```

### Step 4: Generate Dataset

The script automatically generates:

```text
employee_salary_dataset.csv
```

### Step 5: Perform Preprocessing

The processed dataset is saved as:

```text
processed_employee_salary.csv
```

### Step 6: Train the Model

The model is trained using the processed dataset and evaluated on the test set.

### Step 7: Predict Salary

Provide employee details such as:

* Age
* Gender
* Education Level
* Experience
* Skills Score
* Certifications
* Job Role

The system predicts the expected salary.

---

## Key Insights from Analysis

### Experience Influences Salary

Employees with higher years of experience generally receive higher salaries.

### Skills Matter

Employees with higher skills scores tend to earn significantly more.

### Education Impact

Salary generally increases with educational qualifications:

```text
PhD > Master > Bachelor > High School
```

### Job Role Impact

Higher-paying roles include:

* Manager
* Data Scientist
* DevOps Engineer
* Software Engineer

### Company Type Effect

Salary trends observed:

```text
MNC > Government > Startup
```

### Certifications Increase Salary

Employees with more certifications generally earn higher salaries.

---

## Model Performance Summary

The model was evaluated using:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

### Performance Highlights

* High prediction accuracy
* Strong correlation between predicted and actual salary
* Effective handling of both categorical and numerical features
* Robust performance on unseen test data

---

## Future Improvements

* Deploy as a Streamlit Web Application
* Use real-world HR datasets
* Add advanced salary influencing factors
* Compare multiple regression models
* Hyperparameter tuning for improved accuracy
* Integration with recruitment and HR systems

---

## Conclusion

The Employee Salary Prediction System demonstrates a complete Machine Learning workflow from synthetic dataset generation to salary prediction. The project showcases data preprocessing, exploratory data analysis, feature engineering, model training, evaluation, and prediction, making it a practical application of machine learning in Human Resource Analytics.
