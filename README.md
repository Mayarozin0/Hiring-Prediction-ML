#  Candidate Hiring Prediction - Binary Classification Machine Learning Project

This project is a **binary classification model** that predicts whether a job candidate will be hired (1) or not hired (0) based on various candidate features. Developed as part of a **Machine Learning course at Tel Aviv University**, this project scored **100** and showcases advanced techniques in data preprocessing, feature engineering, model selection, and hyperparameter tuning.

## Project Overview

###  Goal
The goal was to create a predictive model that can accurately classify candidates as hired or not hired based on their characteristics, such as:
- Previous work experience
- Technical skills and technology stack
- Education and years of experience
- Demographic details

###  Data and Features
- **Features:** The dataset includes both **numerical** and **categorical features**, covering demographics, technical experience, and other personal attributes.
- **Target Variable:** `hired_status` - 1 (hired) or 0 (not hired)
- **Feature Engineering:** Created additional features such as technology stack count and top technology groups for better prediction accuracy.

## Data Processing & Preprocessing

1. **Missing Values**: Handled using imputation (median for numerical and mode for categorical data).
2. **Outliers**: Detected and removed using IQR and Modified Z-Score methods for skewed distributions, ensuring clean data without extreme values.
3. **Scaling**: Standard scaling was applied to numerical data to improve model performance.
4. **Dimensionality Reduction**: Used **Principal Component Analysis (PCA)** to reduce the datasets dimensionality, retaining 98% of the original variance.

## Models and Approach

The project employed a range of machine learning models to solve the binary classification problem. Each model was fine-tuned using **Grid Search** to identify optimal hyperparameters.

1. **K-Nearest Neighbors (KNN)**
2. **Logistic Regression**
3. **Random Forest Classifier**
4. **Multi-Layer Perceptron (MLP)**

After tuning and evaluation, **MLP (Multi-Layer Perceptron)** was selected as the final model due to its superior balance of accuracy and generalization capability, achieving a high **AUC score** on validation data.

### Model Performance

| Model               | Train AUC | Validation AUC | Overfitting Analysis            |
|---------------------|-----------|----------------|----------------------------------|
| KNN                 | 0.88      | 0.87           | Minimal overfitting              |
| Logistic Regression | 0.86      | 0.86           | Stable and generalizable         |
| Random Forest       | 0.95      | 0.89           | Moderate overfitting             |
| MLP                 | 0.93      | 0.90           | Chosen for high validation AUC   |

### Cross-Validation and ROC Analysis
Cross-validation and **ROC (Receiver Operating Characteristic) curves** were generated for each model. The MLP model consistently achieved the highest AUC across folds, making it the best-performing model for this classification task.

## Notable Techniques

- **Modified Z-Score**: Applied for outlier detection, a method not covered in the course syllabus.
- **Advanced Hyperparameter Tuning**: Experimented with various values for each model to achieve optimal results.
- **Dimensionality Reduction (PCA)**: Reduced the risk of overfitting while preserving data richness.

## Results and Conclusions

The project concluded with a **highly accurate MLP model** that predicts hiring decisions effectively. The model's strong performance in cross-validation and validation AUC underscores its reliability in handling real-world hiring data.

---

## How to Use

1. **Clone the repository** and install the required libraries.
2. **Run the Jupyter Notebook** to load, preprocess, and model the data.
3. **Experiment with different hyperparameters** to observe how they affect model performance.

---

This project demonstrates key machine learning skills, including data preprocessing, feature engineering, model tuning, and validation techniques, making it a valuable showcase for any machine learning role.
