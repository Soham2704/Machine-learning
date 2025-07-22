Titanic Survival Prediction

Objective
The goal of this project is to analyze the classic Titanic dataset and build a machine learning model to predict whether a passenger survived the disaster based on their features.
This is a foundational classification problem in data science.

Dataset
The dataset was sourced from the Kaggle Titanic: Machine Learning from Disaster competition. 

Workflow
The project followed a structured data science workflow:
Data Exploration: Loaded the dataset and performed an initial inspection using .head(), .info(), and .describe() to understand the features, data types, and identify missing values.

Data Cleaning:
Addressed missing data by:
Filling missing Age values with the median age.
Dropping the Cabin column due to a high percentage of missing values.
Filling the two missing Embarked values with the mode.

Feature Engineering:
Created a new FamilySize feature by combining the SibSp (siblings/spouses) and Parch (parents/children) columns to better represent a passenger's family context.

Exploratory Data Analysis (EDA):
Used matplotlib and seaborn to create visualizations and uncover key patterns related to survival.

Model Building:
Converted categorical features (Sex, Embarked) into numerical format.
Split the data into training (80%) and testing (20%) sets.
Trained a DecisionTreeClassifier model on the training data.

Model Evaluation: 
Assessed the model's performance on the unseen test data using accuracy as the primary metric.

Key Findings & Visualizations
EDA revealed several key factors influencing survival:
Sex: Females had a significantly higher survival rate than males.
Passenger Class (Pclass): First-class passengers had a much higher chance of survival compared to third-class passengers.
Age: Children had a higher survival rate than other age groups.

Results
The final DecisionTreeClassifier model achieved a prediction accuracy of ~77% on the test set.
This demonstrates a solid ability to predict passenger survival based on the learned features.

Technologies Used
Python
Pandas
Matplotlib
Seaborn
Scikit-learn
