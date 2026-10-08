# 📊 Sales Prediction using Machine Learning

## 📌 Project Overview

This project is completed as part of the **CodeAlpha Data Science Internship**.

The objective of this project is to develop a machine learning model that predicts product sales based on advertising expenditure across different media channels.

The project uses the **Advertising dataset**, containing advertising spending on **TV, Radio, and Newspaper**, along with the corresponding sales values.

The project covers data cleaning, exploratory data analysis, correlation analysis, feature selection, regression model development, model evaluation, sales prediction, and business insights.

---

## 🎯 Objectives

* Analyze the relationship between advertising expenditure and sales.
* Clean and prepare the dataset for machine learning.
* Explore the influence of different advertising channels on sales.
* Build regression models for sales prediction.
* Compare the performance of multiple machine learning algorithms.
* Identify the most important advertising features.
* Predict sales for a given advertising budget.
* Provide data-driven marketing insights.

---

## 📂 Dataset

The dataset contains **200 records** and the following variables:

| Feature     | Description                               |
| ----------- | ----------------------------------------- |
| `TV`        | Advertising expenditure through TV        |
| `Radio`     | Advertising expenditure through Radio     |
| `Newspaper` | Advertising expenditure through Newspaper |
| `Sales`     | Target variable representing sales        |

The original dataset also contained an `Unnamed: 0` index column, which was removed during data cleaning.

**Dataset source:** Kaggle Advertising Dataset

---

## 🛠️ Technologies and Libraries

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* Jupyter Notebook

---

## 🔄 Project Workflow

```text
Data Collection
      ↓
Data Understanding
      ↓
Data Cleaning
      ↓
Exploratory Data Analysis
      ↓
Correlation Analysis
      ↓
Feature Selection
      ↓
Train-Test Split
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Feature Importance Analysis
      ↓
Sales Prediction
      ↓
Business Insights
```

---

## 🧹 Data Cleaning

The following preprocessing steps were performed:

* Checked the dataset structure and data types.
* Checked for missing values.
* Checked for duplicate records.
* Removed the unnecessary `Unnamed: 0` index column.
* Selected `TV`, `Radio`, and `Newspaper` as input features.
* Selected `Sales` as the target variable.

### Dataset Shape

* Original dataset: **200 rows × 5 columns**
* After removing the unnecessary index column: **200 rows × 4 columns**

There were:

* **0 missing values**
* **0 duplicate rows**

---

## 📊 Exploratory Data Analysis

Exploratory data analysis was performed to understand the relationship between advertising expenditure and sales.

The analysis included:

* Sales distribution
* TV advertising vs Sales
* Radio advertising vs Sales
* Newspaper advertising vs Sales
* Correlation matrix
* Feature importance analysis

### Correlation with Sales

| Advertising Channel | Correlation |
| ------------------- | ----------: |
| TV                  |  **0.7822** |
| Radio               |  **0.5762** |
| Newspaper           |  **0.2283** |

TV advertising showed the strongest linear relationship with Sales among the three advertising channels.

---

## 🤖 Machine Learning Models

Three regression models were trained and evaluated:

1. Linear Regression
2. Decision Tree Regression
3. Random Forest Regression

The dataset was divided into:

* **80% training data:** 160 records
* **20% testing data:** 40 records

---

## 📈 Model Evaluation

The models were evaluated using:

* **MAE (Mean Absolute Error)**
* **RMSE (Root Mean Squared Error)**
* **R² Score**

### Results

| Model             |        MAE |       RMSE |   R² Score |
| ----------------- | ---------: | ---------: | ---------: |
| Linear Regression |     1.4608 |     1.7816 |     0.8994 |
| Decision Tree     |     0.9850 |     1.4748 |     0.9311 |
| **Random Forest** | **0.6201** | **0.7686** | **0.9813** |

### 🏆 Best Model

The **Random Forest Regression** model achieved the best performance.

* **MAE:** 0.6201
* **RMSE:** 0.7686
* **R² Score:** 0.9813

The R² score indicates that the model explains approximately **98.13% of the variation in the test-set sales values**.

---

## ⭐ Feature Importance

Random Forest feature importance was used to understand the relative predictive contribution of each advertising channel.

| Feature   |   Importance |
| --------- | -----------: |
| **TV**    | **0.624810** |
| **Radio** | **0.362201** |
| Newspaper | **0.012989** |

### Key Finding

TV had the highest feature importance, followed by Radio. Newspaper had substantially lower predictive importance in the trained Random Forest model.

---

## 🔮 Sales Prediction

The trained Random Forest model was used to predict sales for the following advertising budget:

|  TV | Radio | Newspaper |
| --: | ----: | --------: |
| 150 |    30 |        20 |

### Predicted Sales

**16.68**

This demonstrates how the trained model can be used to estimate sales for a new advertising budget.

---

## 💡 Business Insights

1. **TV is the most influential advertising feature** in the trained model, with a feature importance of approximately 62.48%.

2. **Radio is also an important predictive feature**, with approximately 36.22% feature importance.

3. **Newspaper has relatively low predictive importance**, with approximately 1.30% feature importance.

4. The **Random Forest model performed better** than Linear Regression and Decision Tree Regression on the test data.

5. Businesses can use machine learning models to estimate expected sales under different advertising budget combinations.

6. The results can support **data-driven advertising budget planning** and marketing decision-making.

---

## 📁 Project Structure

```text
CodeAlpha_SalesPrediction/
│
├── data/
│   └── advertising.csv
│
├── Sales_Prediction.ipynb
│
├── sales_prediction_model.pkl
│
├── requirements.txt
│
└── README.md
```

---

## ▶️ How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/CodeAlpha_SalesPrediction.git
```

### 2. Open the project

```bash
cd CodeAlpha_SalesPrediction
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Open the Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Sales_Prediction.ipynb
```

### 5. Run the notebook

Run the cells sequentially to perform:

* Data preprocessing
* Exploratory data analysis
* Model training
* Model evaluation
* Feature importance analysis
* Sales prediction

---

## 💾 Saved Model

The trained Random Forest model is saved as:

```text
sales_prediction_model.pkl
```

The saved model can be loaded later using Joblib for making predictions on new advertising data.

---

## 📌 Conclusion

This project demonstrates the use of machine learning for sales prediction based on advertising expenditure.

Among the evaluated models, **Random Forest Regression achieved the best performance with an R² score of 0.9813**, making it the best-performing model in this project.

The analysis also showed that **TV and Radio were considerably more important predictive features than Newspaper** in the trained model.

Overall, the project demonstrates how data analysis and machine learning can be applied to support **sales forecasting and data-driven marketing decisions**.

---

## 👩‍💻 Author

**Elaiyarasi E**

Data Science Intern | Aspiring Data Scientist

### Internship

**CodeAlpha — Data Science Internship**

---

