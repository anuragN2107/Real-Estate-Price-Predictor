# 🏡 Real Estate House Price Predictor (Linear Regression Baseline)

![Python](https://img.shields.io/badge/Python-3.12-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Machine_Learning-Scikit--Learn-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

An end-to-end Machine Learning baseline project that predicts house values in King County, Washington, based on physical characteristics. Built entirely inside Google Colab using a standard data science lifecycle workflow.

---

## 💼 Business Problem
Manual property appraisal is slow, expensive, and heavily subjective. Real estate platforms like Zillow or Redfin rely on Automated Valuation Models (AVMs) to provide instant, data-driven property estimates to keep buyers and sellers informed. 

The goal of this project is to build a baseline **Linear Regression model** that quantifies the relationship between core home features and its final sale price.

---

## 📊 Methodology & Workflow

The project follows a highly organized, human-centric data pipeline:

1. **Data Acquisition:** Loaded the King County housing dataset (~21,600 rows).
2. **Data Cleaning:** Implemented **Median Imputation** to seamlessly handle missing data (`NaN` values) in critical feature columns without biasing the distribution.
3. **Exploratory Data Analysis (EDA):** Leveraged a Pearson correlation matrix to isolate features showing the strongest linear relationship with market value.
4. **Data Splitting:** Applied an **80/20 train-test split** to ensure unbiased model evaluation.
5. **Model Fitting:** Trained a multi-variable Linear Regression model to establish baseline performance metrics.

---

## 🔬 Core Features Used
* `sqft_living`: Square footage of the interior living space (Strongest predictor)
* `bedrooms`: Number of bedrooms
* `bathrooms`: Number of bathrooms
* `grade`: Overall grade given to the housing unit, based on King County grading system (1-13)

---

## 📈 Key Findings & Insights

### 1. The Weights (What the Model Learned)
The model assigns explicit financial weights to physical attributes. For example, controlling for other variables, every single square foot of living space (`sqft_living`) systematically scales up the baseline pricing configuration.

### 2. Model Evaluation Metrics
* **$R^2$ Score: ~0.54** * *Insight:* Over half (54%) of the price variations in King County can be predicted purely using just four basic physical characteristics.
* **Mean Absolute Error (MAE): ~$165,000**
  * *Insight:* On average, our baseline model misses the true market value by roughly $165k. While not robust enough for automated high-frequency trading, it creates a perfect foundational baseline.

---

## 🛠️ Tech Stack & Dependencies
* **Google Colab** (Development Environment)
* **Pandas & NumPy** (Data Exploration & Wrangling)
* **Matplotlib & Seaborn** (Data Visualization)
* **Scikit-Learn** (Statistical Modeling & Metrics)

---

## 🚀 How to Run the Project
1. Clone this repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git)
