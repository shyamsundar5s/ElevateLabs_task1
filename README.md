# 🚢 ElevateLabs Task 1 – Titanic Survival Data Preprocessing
This project focuses on cleaning and preprocessing Titanic passenger data for survival prediction. The goal is to prepare the dataset for machine learning models by handling missing values, encoding categorical features, scaling numerical features, and identifying/removing outliers.

## 📁 Repository Contents
ElevateLabs_task1/
├── Titanic_survival.ipynb   # Main notebook with preprocessing steps
├── tested.csv               # Titanic dataset (modified/test variant)
└── README.md                # Project overview and documentation

## 📊 Dataset Description
The dataset `tested.csv` is based on the [Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic) competition, containing passenger information like:
* `PassengerId`: Unique ID
* `Pclass`: Ticket class (1, 2, 3)
* `Name`, `Sex`, `Age`, `SibSp`, `Parch`, `Ticket`, `Fare`, `Cabin`, `Embarked`
* `Survived`: Target variable (0 = No, 1 = Yes)

## 🔧 Preprocessing Steps
The `Titanic_survival.ipynb` notebook includes the following steps:
### 1. Exploratory Data Analysis (EDA)
* Overview of dataset using `.head()`, `.info()`, `.describe()`
* Null values identified using heatmaps and `.isnull().sum()`
### 2. Handling Missing Data
* Filled missing `Age` with median
* Filled `Embarked` with mode
* Dropped `Cabin` column due to excessive nulls
### 3. Categorical Encoding
* Converted `Sex` into binary format (0 = male, 1 = female)
* One-hot encoded `Embarked` into dummy variables
### 4. Feature Scaling
* Standardized `Age` and `Fare` using `StandardScaler` from scikit-learn
### 5. Outlier Removal
* Used IQR method to detect and remove outliers in `Age` and `Fare`
* Visualized with boxplots
### 6. Final Cleaned Dataset
* Dataset was cleaned and transformed for machine learning modeling
* Ready to be used with models like logistic regression, SVM, etc.
