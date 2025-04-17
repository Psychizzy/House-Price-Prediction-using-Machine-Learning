# 🏠 House Price Prediction using Machine Learning

## 👨‍💻 By: Ajayi Oluwaseyi  
📧 Email: oluwaseyi1414@gmail.com  
📂 Project Type: Regression | Supervised Machine Learning  
📌 Tools Used: Python, Pandas, Scikit-Learn, Matplotlib, Seaborn  

---

## 📈 Project Objective

The goal of this project was to build a machine learning model that predicts **house prices** based on several features such as area, number of bedrooms/bathrooms, availability of air conditioning, furnishing status, and more.

We aimed to:

- Build a baseline prediction model using **Linear Regression**
- Try advanced models like **Random Forest** and **Gradient Boosting**
- Tune hyperparameters for performance
- Measure accuracy using **R²**, **MAE**, and **RMSE**
- Visualize actual vs predicted values
- Extract meaningful insights from feature importance

---

## 📦 Dataset Summary

- File: `Housing.csv`  
- Rows: 545  
- Target: `price`  
- Key features: `area`, `bedrooms`, `bathrooms`, `stories`, `airconditioning`, `furnishingstatus`, `mainroad`, etc.

---

## 🔧 Data Preprocessing

- Converted categorical features (`yes/no`) into binary (0/1)
- One-hot encoded `furnishingstatus` to create `semi-furnished` and `unfurnished` flags
- Handled missing values and ensured all data types were model-friendly
- Defined `X` (features) and `y` (target = price)

---

## 🧠 Modeling Process

### 🔹 Linear Regression (Baseline)

- **R²**: 0.65  
- **MAE**: ₦970,043  
- **RMSE**: ₦1,324,506  

✅ Decent baseline — captured basic price patterns but struggled with high-value outliers.

---

### 🔹 Random Forest Regressor

- **R²**: 0.61  
- **MAE**: ₦1,022,560  
- **RMSE**: ₦1,401,496  

❌ Underperformed — possibly overfitting on a small dataset.

---

### 🔹 Gradient Boosting Regressor (Raw)

- **R²**: 0.66  
- **MAE**: ₦960,578  
- **RMSE**: ₦1,299,761  

🔥 Best performance. More stable predictions. Chosen as **final model**.

---

### 🔹 Gradient Boosting (Tuned via GridSearchCV)

- **R²**: 0.62  
- **MAE**: ₦1,016,803  
- **RMSE**: ₦1,373,683  

⚠️ Tuning led to overfitting. Performance dropped. Reverted to raw model.

---

## 🔍 Feature Importance (Top Drivers of Price)

| Rank | Feature           | Why It Matters                            |
|------|-------------------|-------------------------------------------|
| 1️⃣   | `area`            | Larger houses cost more                   |
| 2️⃣   | `bathrooms`       | Indicates comfort and modern design       |
| 3️⃣   | `airconditioning` | Adds value and comfort in hot climates    |
| 4️⃣   | `parking`         | More convenience = more value             |

Least impactful: `furnishingstatus_semi-furnished`

---

## 📊 Visualizations

- Actual vs Predicted price plots
- Feature importance bar chart
- Error metrics printed for comparison
- Scatter plots and residual analysis

---

## 🧠 Final Model Summary

| Model                  | R²    | MAE        | RMSE       |
|------------------------|--------|------------|------------|
| **Gradient Boosting**  | 0.66   | ₦960k      | ₦1.29M     |
| Linear Regression      | 0.65   | ₦970k      | ₦1.32M     |
| Random Forest          | 0.61   | ₦1.02M     | ₦1.40M     |

✅ Final Model: **Gradient Boosting Regressor (raw)**

---

## 💡 Key Learnings

- More complex models don’t always win — sometimes defaults work best
- Feature importance can guide business decisions (e.g. invest in size, not furniture)
- Evaluation metrics (R², MAE, RMSE) must be used together to understand model behavior
- Visualizations are critical for interpreting model success/failure

---

## ✅ Next Steps

- Try larger datasets for better tuning and generalization
- Explore model explainability with SHAP
- Deploy model via a simple web app or API

---

## 🗂 Files Included

- 📄 `house_price_prediction.ipynb` — full Jupyter notebook
- 📦 `Housing.csv` — original dataset
- 📊 `README.md` — this file
- 📸 Screenshots for documentation (optional)

---

## 🔗 Connect

- 📧 Email: oluwaseyi1414@gmail.com  
- 💼 www.linkedin.com/in/ajayi-oluwaseyi-865a35248 
- 📁 https://github.com/Psychizzy  

---

> This project was built as part of a machine learning internship challenge. It represents not just a model, but a journey in building, tuning, evaluating, and storytelling with data.
