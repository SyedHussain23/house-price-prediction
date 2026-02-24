# 🏠 house-price-prediction

This project predicts **residential house prices** using machine learning and advanced feature engineering on the Ames Housing dataset.

It demonstrates a complete **end-to-end regression pipeline**, including:

* Data loading from zipped online dataset
* Missing value handling and preprocessing
* Outlier treatment using IQR capping
* Feature engineering
* Exploratory data analysis (EDA)
* Model training and evaluation
* Business insights and buyer recommendations

The objective is to predict **SalePrice** using 79 explanatory variables describing house characteristics.

---

## 📌 Project Overview

* **Problem Type:** Regression
* **Domain:** Real Estate / Housing Analytics
* **Dataset Size:** 1460 records, 81 features
* **Target Variable:** SalePrice
* **Models Used:** Linear Regression, Decision Tree, Random Forest

---

## 📊 Dataset

The dataset contains detailed residential features such as:

* Property size and quality
* Basement characteristics
* Garage and amenities
* Neighborhood and zoning
* Construction and remodeling history

Dataset Link:
[https://d3ilbtxij3aepc.cloudfront.net/projects/CDS-Capstone-Projects/PRCP-1020-HousePricePred.zip](https://d3ilbtxij3aepc.cloudfront.net/projects/CDS-Capstone-Projects/PRCP-1020-HousePricePred.zip)

---

## 🔧 Data Preprocessing

* Dropped columns with >50% missing values
* Median imputation for numerical features
* Constant imputation (“None”) for categorical features
* One-hot encoding of categorical variables
* Outlier treatment using IQR capping

---

## ⚙️ Feature Engineering

New features created:

* **TotalSF** → Total living space
* **TotalBathrooms** → Combined bathroom count
* **YearsSinceRemodel** → Remodeling recency indicator
* **IsNewHouse** → New construction indicator
* Binary amenity indicators (Garage, Pool, Fireplace, Porch, Deck)

---

## 📈 Exploratory Data Analysis

Key findings:

* Strong positive correlation with SalePrice:

  * OverallQual
  * TotalSF
  * GrLivArea
  * GarageCars
  * GarageArea
* Negative correlation:

  * YearsSinceRemodel
* Amenities positively impact house value
* SalePrice distribution is right-skewed

---

## 🧠 Model Training

Models trained using an 80-20 train-test split:

* Linear Regression (baseline)
* Decision Tree Regressor
* Random Forest Regressor

---

## 📊 Model Evaluation

| Model             | MAE      | RMSE     | R²     |
| ----------------- | -------- | -------- | ------ |
| Linear Regression | 15420.92 | 22129.86 | 0.8998 |
| Decision Tree     | 22199.41 | 33188.32 | 0.7747 |
| Random Forest     | 13576.19 | 20072.77 | 0.9176 |

---

## 🏆 Best Model

**Random Forest Regression** is recommended due to:

* Lowest prediction error (MAE & RMSE)
* Highest R² score
* Ability to capture non-linear relationships and feature interactions

---

## ⚠️ Challenges & Solutions

* High missing values → column removal + imputation
* Outliers → IQR capping
* Categorical variables → one-hot encoding
* Dataset inside zip → extracted using requests + zipfile
* Feature complexity → engineered domain-driven features

---

## 💡 Buyer Insights

* Larger living area and higher construction quality drive higher prices
* Garage and bathroom count significantly influence value
* New or recently remodeled houses are priced higher
* Amenities such as fireplaces and porches add value

---

## 🚀 How to Run

```bash
git clone https://github.com/SyedHussain23/house-price-prediction
cd house-price-prediction
pip install -r requirements.txt
jupyter notebook house-price-prediction.ipynb
```

---

## 👨‍💻 Author

**Syed Hussain Abdul Hakeem**

* GitHub: [https://github.com/SyedHussain23](https://github.com/SyedHussain23)
* LinkedIn: [https://www.linkedin.com/in/syed-hussain-abdul-hakeem](https://www.linkedin.com/in/syed-hussain-abdul-hakeem)

---

## ⭐ Show Your Support

If you found this project useful, consider giving it a ⭐.
