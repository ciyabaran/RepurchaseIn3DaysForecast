
# Project Name: Predicting User Purchases with Machine Learning and LSTM Models

This project utilizes various machine learning algorithms (Random Forest, Logistic Regression, XGBoost) and an LSTM model to predict whether a user will make another purchase within 3 days after their last transaction. The project addresses imbalanced data challenges and highlights the LSTM model's potential for sequential data learning.

## Table of Contents

- [Project Description](#project-description)
- [Technologies Used](#technologies-used)
- [Data Analysis](#data-analysis)
  - [Data Exploration](#data-exploration)
  - [Data Manipulation and Feature Engineering](#data-manipulation-and-feature-engineering)
  - [Data Visualization](#data-visualization)
- [Modeling Approach](#modeling-approach)
  - [Handling Imbalanced Data](#handling-imbalanced-data)
  - [Machine Learning Models](#machine-learning-models)
  - [LSTM Model](#lstm-model)
- [Results and Insights](#results-and-insights)
- [Contact](#contact)

## Project Description

This project aims to develop a user-level model that predicts purchase behavior within 3 days of the last transaction. Despite the challenges posed by highly imbalanced data, the LSTM model demonstrates improved results through parameter optimizations and its ability to learn from sequential data.

## Technologies Used

- **Python**: The primary programming language.
- **Pandas and NumPy**: For data manipulation and numerical operations.
- **Matplotlib and Seaborn**: For data visualization.
- **Scikit-learn**: For implementing machine learning models and performance metrics.
- **XGBoost**: For gradient boosting models.
- **TensorFlow/Keras**: For implementing the LSTM model.
- **SMOTE (Synthetic Minority Over-sampling Technique)**: For addressing data imbalance.

## Data Analysis

### Data Exploration

- **Dataset Overview**: Purchase event data was loaded and examined for structure, types, and missing values.
- **Unique Users**: Identified unique users triggering purchase events.
- **Temporal Analysis**: Incorporated time-based metrics for analysis.

### Data Manipulation and Feature Engineering

- **Data Cleaning**: Removed irrelevant or corrupted metrics.
- **Feature Engineering**: Created new metrics, such as:
  - Total purchases and total purchase amount.
  - Days since the last purchase.
  - Average purchase amount per transaction.
  - Day of the week for purchases.
- **Target Variable**: Defined as 1 if a user made a purchase within 3 days; otherwise, 0.
- **Handling Missing Data**: Cleaned ambiguous data to improve model learning.

### Data Visualization

- Visualized target variable distribution (highly imbalanced data).
- Analyzed relationships between total purchases, purchase gaps, and target behavior.
- Explored weekly patterns and their relation to purchase behaviors.

## Modeling Approach

### Handling Imbalanced Data

- Techniques like SMOTE were applied to mitigate the imbalance in the dataset.
- Optimized hyperparameters using GridSearchCV and RandomizedSearchCV.

### Machine Learning Models

- **Random Forest**: Initial model with parameter tuning using RandomizedSearchCV.
- **Logistic Regression**: Simple model for baseline performance.
- **XGBoost**: More advanced model, performed better with optimized parameters.

### LSTM Model

- Sequential data structured into 3D arrays for LSTM input.
- **Sequence Length**: Set to 5 for capturing sequential user behavior.
- **Class Weights**: Adjusted to improve recall without sacrificing precision.
- Hyperparameter tuning significantly improved LSTM performance, indicating its suitability for the dataset.

## Results and Insights

- **Random Forest and Logistic Regression**: Struggled with recall due to data imbalance but achieved high precision.
- **XGBoost**: Showed improvement over simpler models but still limited by data challenges.
- **LSTM**: Demonstrated the most promising results, with clear potential for further optimization.

## Contact

- **Project Owner**: Çiya Baran Öner
- **Email**: [ciya.baran.oner@gmail.com](mailto:ciya.baran.oner@gmail.com)
- **LinkedIn**: [linkedin.com/in/ciyabaranoner](https://linkedin.com/in/ciyabaranoner)
