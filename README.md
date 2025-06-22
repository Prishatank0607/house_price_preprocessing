# House Price Prediction — Data Preprocessing & Feature Engineering

## About the Project

This project focuses on **data preprocessing and feature engineering** for the Kaggle competition [House Prices: Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques).

The aim is to clean and enrich the dataset before modeling. It involves handling missing values, creating new informative features, encoding categorical data, and preparing a machine learning–ready dataset.

---

## Dataset Overview

The dataset provides **79 features** describing residential homes in Ames, Iowa, and includes the target variable `SalePrice`.

- `train.csv`: 1460 entries with `SalePrice`
- `test.csv`: 1459 entries without `SalePrice`

📌 Dataset Source: [Kaggle - House Prices](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data)

---

## Features Implemented in the Project

-  Loaded and merged train & test sets for uniform processing  
-  Analyzed dataset structure using `.info()` and `.head()`  
-  **Handled missing values** using domain knowledge:
    Replaced categorical NAs with `'None'`
    Filled numeric missing values with `0`, median, or mode  
-  **Feature Engineering**:
    `TotalSF`, `TotalBathrooms`, `Age`, `RemodAge`
    Binary features: `HasPool`, `HasGarage`, `HasFireplace`, `HasBsmt`
-  **Ordinal Encoding** of quality/condition columns using a custom scale  
-  **Label Encoding** of remaining categorical features  
-  Final dataset split into:
    `processed_train.csv`
    `processed_test.csv`  
-  Used clear markdowns and outputs to review each processing step

---

##  Tools and Technologies Used

- **Python 3**
- **Jupyter Notebook**
- **Pandas** for data manipulation
- **NumPy** for numerical processing
- **Scikit-learn** for encoding
- *(Matplotlib & Seaborn — optional for visualization)*

---

## How to Run the Project

```bash
# Clone the repository
git clone https://github.com/Prishatank0607/house_price_preprocessing.git

# Navigate to the project folder
cd house_price_preprocessing

# (Optional) Set up a virtual environment
python -m venv venv
source venv/bin/activate        # macOS/Linux
# venv\Scripts\activate         # Windows

# Install required packages
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook

# Open the notebook
# Select and open the file:
Data preprocessing and feature engineering.ipynb
