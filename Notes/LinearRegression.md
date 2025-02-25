# Linear Regression

In the context of **machine learning**, **clustering**, **classification**, and **regression** are different techniques used for data analysis.  

### 📌 **Clustering**
- **Type**: Unsupervised learning  
- **Goal**: Identify patterns or natural groupings in data without predefined labels.  
- **Example**: Given a set of animal images, a clustering algorithm might group them into "dogs," "cats," and "birds" without knowing these categories beforehand.  
- **Popular algorithms**: K-Means, DBSCAN, Hierarchical Clustering.  

### 🎯 **Classification**
- **Type**: Supervised learning  
- **Goal**: Assign a category (or class) to an input based on labeled training examples.  
- **Example**: Identifying whether an email is "spam" or "not spam" based on historical labeled data.  
- **Popular algorithms**: Decision Trees, Random Forest, Neural Networks, SVM.  

### 📈 **Regression**
- **Type**: Supervised learning  
- **Goal**: Predict a continuous numerical value based on input variables.  
- **Example**: Estimating house prices based on size and location.  
- **Popular algorithms**: Linear Regression, Polynomial Regression, Neural Networks, SVR.  

### 🔍 **Key Differences**
| Feature       | Clustering  | Classification | Regression |
|--------------|------------|---------------|------------|
| Learning Type | Unsupervised | Supervised | Supervised |
| Objective | Group data into unknown clusters | Assign predefined classes | Predict a continuous value |
| Example | Customer segmentation | Medical diagnosis (sick/healthy) | Temperature prediction |
| Output Type | Unknown groups | Predefined categories | Numeric value |

---

### 📌 **Outline: Linear Regression**  

#### **1. Univariate Linear Regression**  
- **Definition**: A linear model with one independent variable (feature). The hypothesis function is:  
  \[
  h(x) = \theta_0 + \theta_1 x
  \]  
- **Cost (Loss) Function - Mean Squared Error (MSE)**  
  \[
  J(\theta) = \frac{1}{2m} \sum_{i=1}^{m} (h(x_i) - y_i)^2
  \]  
  - Measures the average squared differences between predictions and actual values.  
- **Cost Function Convergence**  
  - Goal: Find optimal values of \(\theta_0\) and \(\theta_1\) that minimize \(J(\theta)\).  
  - If the learning rate is too high, the function may not converge.  
- **Gradient Descent Algorithm**  
  - Iteratively updates parameters using the gradient of the cost function:  
    \[
    \theta_j := \theta_j - \alpha \frac{\partial}{\partial \theta_j} J(\theta)
    \]  
  - Learning rate (\(\alpha\)) controls step size.  

#### **2. Multivariate Linear Regression**  
- **Definition**: A linear model with multiple independent variables (features). The hypothesis function is:  
  \[
  h(x) = \theta_0 + \theta_1 x_1 + \theta_2 x_2 + \dots + \theta_n x_n
  \]  
- **Overfitting Problem**  
  - Occurs when the model fits training data too well but performs poorly on new data.  
  - High variance leads to poor generalization.  

#### **3. Regularization - A Way to Deal with Overfitting**  
- **Definition**: Adds a penalty term to the cost function to prevent overfitting.  
- **Common Types**:  
  - **Lasso Regression (L1 Regularization)**:  
    \[
    J(\theta) = \frac{1}{2m} \sum (h(x_i) - y_i)^2 + \lambda \sum |\theta_j|
    \]  
    - Shrinks some coefficients to zero (feature selection).  
  - **Ridge Regression (L2 Regularization)**:  
    \[
    J(\theta) = \frac{1}{2m} \sum (h(x_i) - y_i)^2 + \lambda \sum \theta_j^2
    \]  
    - Reduces magnitude of coefficients without eliminating them.  

---

Distinction between **classification** and **regression**: 

### 📌 **Key Difference**:  
- **Classification**: The output (label) is a discrete integer (e.g., 0 or 1 for binary classification, or multiple categories for multiclass classification).  
- **Regression**: The output (label) is a continuous real number.  

### **Examples of Regression Problems**  
✅ **Weather Forecast** – Predicting temperature, rainfall, or humidity levels.  
✅ **Predicting Wind Velocity** – Using temperature, humidity, and air pressure as features.  
✅ **Stock Market Prediction** – Forecasting stock prices over time (time series analysis).  
✅ **Sales Prediction** – Estimating future sales based on marketing spend.  

---

### 📌 **Supervised Learning – Regression**  

#### **Why is Regression Important in Data Science?**  
1️⃣ **Identifies relationships between variables** – Helps understand how one variable affects another.  
2️⃣ **Enables predictions** – Uses historical data to predict future values.  
3️⃣ **Evaluates model performance** – Measures how well the model fits the data.  

#### **What is Regression?**  
Regression is a **statistical technique** used in data science to analyze and model the **relationship between variables**. It helps in:  
- Understanding correlations  
- Forecasting future trends  
- Optimizing decision-making  