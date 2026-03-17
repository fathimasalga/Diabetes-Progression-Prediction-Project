# Diabetes Progression Prediction using ANN (Deep Learning)

## Project Overview

This project applies **Artificial Neural Networks (ANN)** to predict the progression of diabetes using the **Diabetes dataset from sklearn**.

The objective is to model the relationship between medical predictor variables and disease progression to understand how different factors influence diabetes outcomes.

This is a **regression-based deep learning project** implemented using TensorFlow/Keras.

---

## Dataset

- Source: `sklearn.datasets.load_diabetes()`
- Total Samples: 442
- Features: 10 numerical medical attributes
- Target Variable: Continuous measure of diabetes progression (one year after baseline)

All features are standardized in the dataset.

---

## Project Workflow

### 1️. Data Loading & Inspection
- Loaded dataset from sklearn
- Converted into pandas DataFrame
- Checked structure, shape, and statistical summary
- Verified absence of missing values

### 2️. Exploratory Data Analysis (EDA)
- Distribution analysis of target variable
- Univariate analysis of numerical features
- Correlation heatmap
- Identified moderate relationships between BMI, BP, and disease progression

### 3️. Data Preprocessing
- Feature & target separation
- Standardization using `StandardScaler`
- Train-test split (80% training, 20% testing)

### 4️. Model Building – ANN
- Sequential Neural Network
- Hidden layers with ReLU activation
- Linear output layer (Regression)
- Optimizer: Adam
- Loss Function: Mean Squared Error (MSE)

### 5️. Model Evaluation

Performance Metrics Used:
- Mean Squared Error (MSE)
- R² Score

---

## Results

| Model          | MSE     | R² Score |
|---------------|---------|----------|
| Baseline ANN  | 2812.10 | 0.4692   |
| Improved ANN  | 2761.09 | 0.4789   |

After hyperparameter tuning:
- Increased hidden layers
- Adjusted neuron count
- Reduced learning rate
- Increased training epochs

The improved model achieved better generalization and reduced prediction error.

---

## Key Insights

- ANN successfully captured non-linear relationships in medical data.
- Hyperparameter tuning improved performance moderately.
- The model explains approximately **47–48% of variance** in diabetes progression.
- Deep learning can be effectively applied to healthcare regression problems.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras

---

## Conclusion

This project demonstrates the application of Artificial Neural Networks for regression analysis in healthcare datasets. The improved ANN model achieved better predictive performance through architectural tuning and hyperparameter optimization.

