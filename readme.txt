### Languages and Tools

- **Python**: For data cleaning, analysis, and model building.
- **Pandas**: For data manipulation.
- **Scikit-learn**: For building KNN and Decision Tree models.
- **Matplotlib/Seaborn**: For data visualization.
- **Jupyter Notebook**: Development environment for Python code.

# Online Shoppers Purchasing Intention Prediction

## Overview

This project involves predicting online shopping behavior based on data gathered from the UCI Machine Learning Repository. The goal is to classify whether a shopper will complete a purchase during a session or not, based on various features like page duration, bounce rates, and visitor type. The project follows the key steps of data preparation, exploration, and modeling, utilizing K-Nearest Neighbors (KNN) and Decision Tree algorithms to build predictive models.

### Key Features

1. **Data Preparation**:
   - The dataset includes 12,330 online sessions, with 84.5% classified as "negative" (no purchase) and the rest as "positive" (purchase completed).
   - Data cleaning involved handling outliers for numerical attributes and encoding categorical attributes to make them compatible with machine learning algorithms.
   - A boxplot and the interquartile range (IQR) method were used to detect and address outliers. Categorical attributes such as `VisitorType`, `Weekend`, and `Month` were one-hot encoded.

2. **Data Exploration**:
   - Descriptive statistics were calculated for each attribute, and relationships between the attributes were explored.
   - Several visualizations such as violin plots, line charts, and pie charts were generated to examine patterns between categorical and continuous variables.
   - Relationships between the number of pages visited, time spent on pages, and purchasing behavior were explored.

3. **Feature Selection and Modeling**:
   - A greedy search algorithm was used to select the best subset of features for modeling.
   - Both K-Nearest Neighbors (KNN) and Decision Tree models were trained on the dataset. Cross-validation was used to fine-tune the parameters.
   - Model performance was compared, with KNN achieving slightly lower accuracy but higher precision for predicting true revenues, while Decision Tree had better recall.

### System Design and Methodology

1. **Data Preparation**:
   - Outliers were identified and handled using the interquartile range (IQR) method. The decision to retain or replace outliers depended on their impact on the target variable, `Revenue`.
   - Categorical attributes were one-hot encoded to make them usable by KNN and Decision Tree algorithms.

2. **Exploratory Data Analysis (EDA)**:
   - Descriptive statistics and visualizations such as boxplots, line charts, and pie charts were used to understand the distribution of attributes and their relationships with the target variable.
   - The relationship between visitor behavior (e.g., page views, bounce rates) and purchasing intention was closely examined.

3. **Feature Selection and Model Training**:
   - Feature selection was performed using a greedy search algorithm to find the subset of features that maximized model performance.
   - KNN and Decision Tree models were trained, and cross-validation was used to select optimal hyperparameters for both models.

### Tasks and Results

1. **Task 1: Data Cleaning and Preparation**:
   - Cleaned the dataset by removing or correcting outliers and encoding categorical variables.
   
2. **Task 2: Data Exploration**:
   - Explored the relationship between attributes like page duration, bounce rates, and visitor types with the likelihood of completing a purchase.
   - Visualized the behavior of returning and new visitors to understand how their browsing patterns differ.

3. **Task 3: Model Building and Evaluation**:
   - Both KNN and Decision Tree models were built, achieving accuracies of around 88%.
   - Decision Tree outperformed KNN in recall, while KNN had better precision for predicting positive purchases.

### Files in the Repository

- **`code.ipynb`**: Jupyter Notebook containing the Python code for data preparation, feature selection, model building, and evaluation.
- **`report.pdf`**: Detailed report describing the data cleaning, exploration, feature selection, and model evaluation process.
- **`dataset.zip`**: The original dataset used for the analysis.

### How to Run the Project

1. **Set Up Jupyter Notebook**:
   - Install Anaconda and open the `code.ipynb` notebook in Jupyter.
   
2. **Run the Notebook**:
   - Execute the cells to clean the data, explore the dataset, and build the KNN and Decision Tree models.
   
3. **View the Report**:
   - Open `report.pdf` to view a detailed explanation of the data cleaning, exploration, and modeling process.

### Data Source

The dataset used in this project is publicly available on the UCI Machine Learning Repository, under the "Online Shoppers Purchasing Intention Dataset". The data includes sessions of users who visited an online shopping website, with features such as page types, visitor information, and browsing patterns.
