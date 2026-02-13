# 🚢 Titanic Survival Prediction

## 📌 Project Overview
This project involves analyzing the famous **Titanic dataset** to predict passenger survival. The goal is to identify factors that contributed to survival rates and build a Machine Learning model to classify passengers as survivors or non-survivors.

## 🛠️ Tools & Libraries Used
* **Python 3**
* **Pandas & NumPy:** For data manipulation and linear algebra.
* **Matplotlib & Seaborn:** For data visualization and correlation heatmaps.
* **Scikit-Learn:** For preprocessing (StandardScaler) and Machine Learning (Random Forest).

## 📊 Key Steps in Analysis

### 1. Data Cleaning & Preprocessing
* **Handling Missing Values:**
    * `Age`: Filled with the **mean**.
    * `Fare`: Filled with the **median**.
    * `Embarked`: Filled with the **mode**.
* **Dropping Columns:** Removed non-predictive columns like `Cabin`, `Name`, `Ticket`, and `PassengerId`.
* **Encoding:** Converted categorical variables (`Sex`, `Embarked`) into numerical format using Mapping and One-Hot Encoding.
* **Scaling:** Applied `StandardScaler` to `Age` and `Fare` for better model performance.

### 2. Feature Engineering
* Created a new feature called **`FamilySize`** by combining `SibSp` (Siblings/Spouses) and `Parch` (Parents/Children) to understand if traveling alone or with family impacted survival.

### 3. Exploratory Data Analysis (EDA)
* Visualized correlations between features using a **Heatmap** to identify important relationships (e.g., correlation between Sex/Class and Survival).

### 4. Machine Learning Model
* **Algorithm:** Random Forest Classifier.
* **Setup:** Used 100-300 estimators with specific depth constraints to prevent overfitting.
* **Evaluation:**
    * Achieved an **Accuracy of ~82%** on the validation set.
    * Analyzed Feature Importance to see which factors mattered most.

## 📈 Results & Insights
* **Gender (`Sex`)** was the most significant factor in survival prediction (Females had a higher chance of survival).
* **Passenger Class (`Pclass`)** and **Fare** also played crucial roles.
* The model successfully generated predictions for the test dataset (`final_predictions.csv`).

## 🚀 How to Run
1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
