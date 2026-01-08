🏠 **Hyderabad House Price Prediction using Machine Learning**
📌 Project Overview:
This project focuses on building a machine learning regression model to predict house prices in Hyderabad based on key property features such as location, built-up area, BHK, building status, and market trends.
The goal is to assist buyers, sellers, and analysts in estimating realistic property prices using data-driven insights.

🎯 Problem Statement:
Real estate prices vary significantly based on locality, property size, and market demand.
Manual price estimation is often inaccurate and subjective.
This project aims to predict house prices (in Lakhs) using machine learning by analyzing historical housing data from Hyderabad.

*** Dataset Description***
Rows: 3660
Target Variable: price(L)

**Features Used:**
**location – Property locality

area_insqft – Built-up area

bhk – Number of bedrooms (engineered feature)

building_status – Ready to move / Under construction

rate_persqft (used only for EDA, not final training to avoid leakage)

🔍**** Exploratory Data Analysis (EDA)****

Key insights discovered:
Rate per square foot has the strongest correlation with price
Location significantly impacts house prices
Area shows a moderate positive relationship with price
Building status affects affordability
Data is right-skewed, which is expected in real estate datasets

**Visualizations include:**

Scatter plots (Price vs Area, Price vs Rate per Sqft)

Box plots (Outlier detection)

Location-wise price distribution

🧹** Data Preprocessing**

Removed unnecessary columns

Verified data consistency using derived price per sqft

Handled outliers selectively (no blind removal)

Extracted numerical BHK feature from text

Scaled numerical features

One-hot encoded categorical variables

Used pipelines to prevent data leakage

** Feature Engineering**

Extracted bhk from property title

Validated pricing consistency using derived features

Excluded leakage-prone features from final model

**Model Used**

Gradient Boosting Regressor

Handles non-linear relationships well

Performs effectively on structured tabular data

**Pipeline includes:**

ColumnTransformer (scaling + encoding)

Gradient Boosting regression model

📊 **Model Evaluation**

**Evaluation Metrics:**

R² Score

Mean Absolute Error (MAE)

The final model achieves strong predictive performance while maintaining realistic generalization by avoiding data leakage.

** Technologies & Libraries***

Python

Pandas, NumPy

Matplotlib

Scikit-learn

Jupyter Notebook

📌 Key Learnings

Importance of avoiding data leakage in ML projects

Feature engineering significantly improves model performance

Real estate pricing is influenced more by location and rate per sqft than size alone

Pipelines ensure clean and reproducible ML workflows

🔮 Future Enhancements

Try XGBoost / LightGBM

Apply target encoding for high-cardinality locations

Log transformation of target variable

Deploy model as a web application

📁 Project Structure
├── data/
│   └── Hyderabad_House_Price.csv
├── notebooks/
│   └── EDA_and_Modeling.ipynb
├── README.md
└── requirements.txt

👩‍💻 Author

Kothuri Srujana
Machine Learning & Data Science Enthusiast

⭐ If you like this project, feel free to star the repository!
