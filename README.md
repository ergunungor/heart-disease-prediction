# heart-disease-prediction
A Machine Learning project predicting heart disease using Linear Regression with thresholding logic. Achieved ~93% accuracy.

# 🫀 Heart Disease Prediction

This project implements a machine learning model to predict the presence of heart disease in patients based on various clinical attributes.

## 🚀 Project Overview
The goal of this project is to analyze medical data and determine whether a patient has heart disease (Presence) or not (Absence). 

Although this is a classification problem (Yes/No), this project demonstrates an experimental approach using **Linear Regression**. By applying a threshold to the continuous output of the regression model, we successfully converted the predictions into binary classes with high accuracy.

## 📊 Dataset Features
The model is trained on clinical features including:
* **Age:** Patient's age.
* **Sex:** Patient's gender.
* **Chest Pain Type:** (Critical Feature) The type of chest pain experienced.
* **BP:** Resting blood pressure.
* **Cholesterol:** Serum cholesterol levels.
* **FBS over 120:** Fasting blood sugar > 120 mg/dl.
* **Max HR:** Maximum heart rate achieved.
* **ST Depression:** Induced by exercise relative to rest.
* **Slope of ST:** The slope of the peak exercise ST segment.
* **Thallium:** Thallium stress test result.
* **Target:** Heart Disease Presence (1) or Absence (0).

## 🛠️ Methodology & Approach

1.  **Data Preprocessing:**
    * Target labels were converted to numerical format (Label Encoding).
    * Crucial features, such as "Chest Pain Type", were ensured to be included in the training set.

2.  **Model Selection:**
    * **Algorithm:** Linear Regression (Scikit-Learn).
    * **Logic:** Since Linear Regression outputs continuous numbers, a **Thresholding Logic** was applied:
        * Prediction > 0.5 $\rightarrow$ **1 (Heart Disease)**
        * Prediction $\leq$ 0.5 $\rightarrow$ **0 (Healthy)**

3.  **Evaluation:**
    * Instead of using the $R^2$ score (which is misleading for this specific approach), **Accuracy Score** was used to evaluate performance.

## 📈 Results

* **Model Accuracy:** **~92.59%**
* **Key Insight:** While the statistical $R^2$ score was lower (~0.52), the model proved highly effective at distinguishing between healthy and sick patients when the output was rounded to the nearest class.

## 💻 Installation & Usage

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/heart-disease-prediction.git](https://github.com/YOUR_USERNAME/heart-disease-prediction.git)
    ```

2.  **Install Dependencies:**
    ```bash
    pip install pandas numpy scikit-learn
    ```

3.  **Run the Notebook:**
    Open `heart_disease_prediction.ipynb` to view the analysis and model training steps.

---
*Developed by Ergün Üngör*
