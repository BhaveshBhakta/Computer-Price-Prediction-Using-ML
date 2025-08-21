## Computer Price Prediction

### Project Overview

This project aims to **predict the price of laptops** based on a variety of technical specifications. By analyzing features such as the company, product type, screen size, CPU, RAM, storage, GPU, and operating system, the goal is to develop a regression model that can accurately estimate a laptop's price. This can be a valuable tool for consumers, retailers, and market analysts.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Laptop Price](https://www.kaggle.com/datasets/muhammetvarl/laptop-price)
  * **Size**: 1303 entries, 13 columns. After data cleaning and outlier removal, the dataset size is reduced.
  * **Key Features**:
      * `Company`, `Product`, `TypeName`, `Inches`, `ScreenResolution`, `Cpu`, `Ram`, `Memory`, `Gpu`, `OpSys`, `Weight`.
  * **Approach**:
      * **Data Cleaning**: Dropped `laptop_ID` as it's a unique identifier. Removed outliers using the Interquartile Range (IQR) method on numerical columns. Cleaned and converted `Ram` and `Weight` columns to numerical types.
      * **Exploratory Data Analysis**: Histograms and boxplots were used for visualization to understand data distributions and the relationship between different features and price.
      * **Label Encoding**: Applied to all columns, including categorical features and the target `Price_euros`.
      * **Regression Task**: The target variable is `Price_euros`.
      * **Models Used**:
          * Linear Regression, Ridge, XGBoost Regressor, Random Forest Regressor, AdaBoost Regressor, Gradient Boosting Regressor, Bagging Regressor, Decision Tree Regressor, SVR, K-Nearest Neighbors Regressor.
  * **Best R² Score**:
      * **0.912** with XGBoost Regressor.
      * **0.894** with Bagging Regressor.
      * **0.888** with Gradient Boosting Regressor.
      * The high R² scores indicate that the models are highly effective at predicting laptop prices based on their specifications.

-----

### Purpose and Applications

  * Help consumers **estimate the fair price of a laptop** based on its specifications.
  * Assist retailers and manufacturers in **competitive pricing strategies**.
  * Identify which technical specifications have the most significant impact on a laptop's price.
  * Support data-driven market analysis and product development in the electronics industry.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Computer-Price-Prediction-Using-ML.git
cd Computer-Price-Prediction-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Re-evaluating the preprocessing step of applying Label Encoding to numerical features; consider using standard scaling for numerical features and only applying encoding to truly categorical ones.
  * Performing comprehensive hyperparameter tuning and cross-validation for all regression models to maximize predictive performance.
  * Exploring advanced feature engineering techniques from the `ScreenResolution` and `Cpu` columns.
  * Adding explainability (e.g., SHAP or LIME) to understand which laptop features are the most significant drivers of price.
