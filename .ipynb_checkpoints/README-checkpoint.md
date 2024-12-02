
# Car Data Analysis Project

## DataBase - CarPrice
/kaggle/input/carprice/CarPrice.csv
[Kagle](https://www.kaggle.com/datasets/goyalshalini93/car-data)
[Kagle](https://www.kaggle.com/datasets/lainguyn123/australia-car-market-data/data)

## Overview of Project

**Objective**: Analyze the Car Data dataset to explore insights and build predictive models. The goal is to understand patterns in car pricing, identify trends, groupings, and recommend the best model for predicting car prices.

**Dataset Details**: The dataset includes attributes such as price, year, fuel type, transmission, mileage, engine size, etc.

**Key Questions**:
- What factors most influence car prices?
- Can we predict car prices using regression models?
- Are there specific clusters of cars based on attributes like mileage or fuel type?
- Can we group cars based on their features (Clustering)?

---

## Exploratory Data Analysis (EDA)

Conduct a thorough analysis to uncover patterns and relationships in the data:

**Data Cleaning**:
- Handle missing or incorrect values (e.g., null mileage, outliers in price).
- Remove or cap outliers (e.g., extremely high/low prices or mileage).
- Check for duplicate records and remove if necessary.

**Feature Transformation**:
- Convert categorical variables (e.g., Fuel_Type, Transmission) into dummy/encoded variables.
- Scale numerical features (e.g., Mileage, Engine_Size) using Min-Max or StandardScaler for Clustering models.

**Descriptive Statistics**:
- Summary statistics for numerical features (mean, median, range, standard deviation).
- Frequency counts for categorical features.

**Visualization**:
- Boxplots to identify outliers in Price, Mileage, etc.
- Heatmap of correlations to see relationships between numerical variables.
- Scatterplots (e.g., Year vs. Price or Mileage vs. Price) to visualize trends.

**Insights**:
- Which features have the strongest correlation with car price?
- Any notable trends (e.g., newer cars costing more, or higher mileage leading to lower prices)?

---

## Models

### 3.1. Model 1: Clustering

**Objective**: Group cars based on similar attributes to identify distinct segments.

**Features for Clustering**:
- Select relevant features: Mileage, Engine_Size, Year, Price.
- Normalize the features to ensure equal weight in clustering.

**Clustering Algorithm**:
- Use K-Means Clustering:
  - Determine the optimal number of clusters (k) using the Elbow Method.
- Alternative: DBSCAN for density-based clustering.

**Output**:
- Visualize clusters with a scatter plot (e.g., Mileage vs. Price).
- Analyze cluster characteristics (e.g., economy cars vs. luxury cars).

**Insights**:
- How do the clusters align with pricing and features?
- What actionable insights can dealerships derive from these segments?

---

### 3.2. Model 2: Regression

**Objective**: Predict car prices based on features.

**Features for Regression**:
- Use features such as Year, Mileage, Engine_Size, Fuel_Type, and Transmission.

**Regression Algorithms**:
- Linear Regression as a baseline model.
- Random Forest Regressor or Gradient Boosting (e.g., XGBoost) for non-linear relationships.

**Train-Test Split**:
- Split the dataset into training and testing sets (e.g., 80-20 split).

**Evaluation**:
- Metrics: Use R², Mean Absolute Error (MAE), and Mean Squared Error (MSE).
- Cross-validate to ensure robustness.

**Feature Importance**:
- Identify which features have the greatest impact on car prices.

---

### 3.3. Optional Additional Model – Classification

**Objective**: Classify cars into price ranges (e.g., low, medium, high).

**Method**:
- Use Decision Trees or Naïve Bayes for classification.
- Evaluate accuracy, precision, and recall metrics.

**Insights**:
- Help categorize cars into meaningful segments for pricing or marketing strategies.

---

## Best Model

**Clustering**:
- Present cluster visualizations and explain characteristics.
- Provide insights into how clusters can help in decision-making (e.g., targeting different customer segments).

**Regression**:
- Report evaluation metrics for all regression models.
- Compare models and choose the best-performing one (e.g., Random Forest for non-linear data). Choose the model with the lowest MAE/MSE and highest R² on the test set.
- Discuss why the selected model performs better (e.g., it captures non-linear relationships, handles categorical features well).

---

## Learning / Challenges

**Learning**:
- Gained insights into data preparation and visualization.
- Learned how different models behave and their strengths/weaknesses for regression tasks.
- Improved skills in handling categorical data, scaling, and feature selection.

**Challenges**:
- Handling missing data or outliers in features like Mileage and Price.
- Balancing model complexity and interpretability.
- Computational time for training advanced models like Gradient Boosting on large datasets.

---

## Final Deliverables

- **Code/Notebook**: Python notebook with detailed steps for EDA, Clustering, and Regression.