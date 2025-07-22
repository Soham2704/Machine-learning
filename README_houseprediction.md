House Price Prediction (Advanced Regression)
Objective
The goal of this project is to build an advanced regression model to accurately predict the sale price of houses in Ames, Iowa. 
This project demonstrates a comprehensive approach to a complex dataset with a large number of features.

Dataset
The dataset was sourced from the Kaggle House Prices: Advanced Regression Techniques competition.

Workflow
The project followed a structured data science workflow:
Data Exploration: Loaded the dataset (80+ features) and performed an initial inspection to understand the data structure, identify a large number of missing values, and analyze the distribution of the target variable, SalePrice.
Exploratory Data Analysis (EDA): Used matplotlib and seaborn to visualize key relationships between important features and the sale price.

Data Cleaning & Feature Engineering:
Dropped columns with a very high percentage of missing values (Alley, PoolQC, etc.).
Systematically filled missing values for numerical columns (e.g., LotFrontage) with the median.
Imputed missing values for categorical columns (e.g., garage-related features) with appropriate placeholders like 'None' or 0.
Used pd.get_dummies to convert all categorical features into a numerical format suitable for modeling.

Model Building:
Separated the data into features (X) and the target (y).
Split the data into training (80%) and testing (20%) sets.
Trained a powerful RandomForestRegressor ensemble model, which combines 100 decision trees to improve predictive accuracy.

Model Evaluation:
Assessed the model's performance on the unseen test data using Root Mean Squared Error (RMSE) as the primary metric.

Key Findings & Visualizations
EDA confirmed several strong relationships with the sale price:
Overall Quality: There is a clear positive relationship between the OverallQual of a house and its final SalePrice.
Living Area: GrLivArea has a strong, linear positive correlation with SalePrice. Larger houses consistently sell for more.

Results
The final RandomForestRegressor model achieved a Root Mean Squared Error (RMSE) of ~$28,400 on the test set. 
This indicates that, on average, the model's predictions are within about $28,400 of the actual sale price, demonstrating strong performance on a complex regression task.

Technologies Used:
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
