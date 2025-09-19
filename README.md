# 🏠 Interactive House Price Prediction Model

This project contains a simple, end-to-end machine learning model for predicting house prices. The entire workflow is captured in a single Jupyter Notebook (`Asthra_Workshop.ipynb`). The model is trained on a synthetically generated dataset and provides an interactive command-line interface for users to get price predictions for new houses based on their features.

---

## ✨ Project Workflow Breakdown

This project follows a systematic approach, broken down into the following steps within the notebook:

### **Step 1: Import Libraries**
-   The necessary Python libraries are imported, including **pandas** for data manipulation, **numpy** for numerical operations, **matplotlib** and **seaborn** for data visualization, and **scikit-learn** for building and evaluating the machine learning model.

### **Step 2: Create a Realistic Dataset**
-   A synthetic dataset of 200 houses is generated to simulate a real-world scenario.
-   The features include `Size_sqft`, `Bedrooms`, and `Age_years`.
-   A formula is used to calculate the `Price_USD`, with added random noise to make it more realistic.

### **Step 3: Basic Dataset Info**
-   Initial exploration is done using `df.info()` to check data types and null values, and `df.describe()` to get summary statistics (mean, median, standard deviation, etc.) for each feature.

### **Step 4: Exploratory Data Analysis (EDA)**
-   Visualizations are created to understand the data's characteristics and relationships:
    -   **Price Distribution**: A histogram shows the frequency distribution of house prices.
    -   **Pairwise Relationships**: A pair plot visualizes the relationships between every pair of features.
    -   **Correlation Heatmap**: A heatmap shows the correlation coefficients between features, indicating which variables have the strongest relationship with the price.

### **Step 5: Prepare Data for Modeling**
-   The dataset is split into features (**X**: `Size_sqft`, `Bedrooms`, `Age_years`) and the target variable (**y**: `Price_USD`).
-   This data is then divided into a **training set (80%)** and a **testing set (20%)** to train the model and test its performance on unseen data.

### **Step 6: Train Linear Regression Model**
-   A `LinearRegression` model from scikit-learn is instantiated.
-   The model is trained using the `.fit()` method on the training data (`X_train` and `y_train`).

### **Step 7: Make Predictions on Test Data**
-   The trained model is used to predict house prices for the test set (`X_test`).
-   The predictions are compared with the actual prices (`y_test`) to see how well the model performs.

### **Step 8: Evaluate Model Performance**
-   The model's accuracy is quantitatively measured using two key metrics:
    -   **Mean Squared Error (MSE)**: Measures the average of the squares of the errors. A lower value is better.
    -   **R-squared (R²)**: Indicates the proportion of the variance in the dependent variable that is predictable from the independent variable(s). A value closer to 1 is better.

### **Step 9: Visualize Predictions vs. Actuals**
-   A scatter plot is generated to visually compare the **Actual Prices** against the **Predicted Prices**.
-   A diagonal line representing a perfect prediction is drawn for reference. The closer the data points are to this line, the better the model's predictions.

### **Step 10: Analyze Model Coefficients**
-   The coefficients of the linear regression model are examined. These values explain the impact of each feature on the house price.
-   For example, a positive coefficient for `Size_sqft` means the price increases as the size increases, while a negative coefficient for `Age_years` means the price decreases as the house gets older.

### **Step 11: Predict New House Price from User Input**
-   An interactive loop is created that prompts the user to enter the **size**, **number of bedrooms**, and **age** of a house.
-   The model then uses this input to predict the house's price in real-time.

---

## 🛠️ Technologies Used

-   Python
-   Pandas & NumPy
-   Matplotlib & Seaborn
-   Scikit-learn
-   Jupyter Notebook
