💻 Laptop Price Predictor

A Machine Learning regression project that predicts laptop prices based on specifications like brand, processor, RAM, storage, GPU, and operating system.


📌 Project Overview

This project builds a machine learning model to predict laptop prices (in Euros) using real-world data from Kaggle. It covers the full ML pipeline — from data cleaning and feature engineering to model comparison and deployment via a Flask web app.


📂 Dataset

- Source: [Kaggle - Laptop Price Dataset](https://www.kaggle.com/datasets/muhammetvarl/laptop-price)
- File: `laptop_price.csv`
- Type: Real-world data (laptop specs and prices scraped from e-commerce platforms)


🔧 Tech Stack

- Language: Python
- Libraries: NumPy, Pandas, Scikit-learn, Pickle
- Web Framework: Flask
- Tools: Jupyter Notebook, VS Code


🚀 Project Workflow

1. Data Cleaning & Feature Engineering
- Removed units from `Ram` and `Weight` columns
- Extracted `Touchscreen` and `IPS` features from `ScreenResolution`
- Grouped rare laptop brands into `Other` category
- Extracted and simplified CPU, GPU, and OS categories
- Dropped irrelevant columns

2. Outlier Handling
- Grouped rare/low-frequency brands into an `"Other"` category
- Removed uncommon GPU types (e.g., ARM) to keep data consistent

### 3. Model Building & Comparison

Trained and compared multiple regression algorithms:

| Model | Algorithm |
|---|---|
| Linear Regression | Baseline model |
| Lasso Regression | Regularized linear model |
| Decision Tree | Tree-based model |
| Random Forest | Ensemble model ✅ Best |

4. Hyperparameter Tuning & Cross Validation
- Used **GridSearchCV** with **5-fold cross validation** to tune Random Forest hyperparameters
- Parameters tuned: `n_estimators` and `criterion`
- Best model saved using **Pickle**

5. Deployment
- Built a simple web application using Flask
- Users can input laptop specifications and get a predicted price in real time


📊 Results

- Best Model: Random Forest Regressor
- Tuning Method: GridSearchCV with 5-Fold Cross Validation
- Deployment: Flask Web Application


🙋‍♂️ Author

Chathupama Kavishya
Undergraduate Student | Machine Learning Enthusiast

- 🔗 [LinkedIn](https://www.linkedin.com/in/chathupama-kavishya-7523b6331/)
- 💻 [GitHub](https://github.com/Ckavishya)
