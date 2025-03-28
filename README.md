# Earthquake Disaster Relief Non-Profit Website

## Overview
This project is a **non-profit website** designed to provide disaster relief support during earthquakes. The website follows a **brown and teal style** to create a trustworthy and calming user experience. It aims to help affected individuals find assistance, connect with relief organizations, and facilitate donations for relief efforts.

## Features
- **Homepage**: Provides essential information about earthquake relief efforts.
- **Donation Portal**: Securely accepts donations to support affected communities.
- **Emergency Contact Page**: Displays key emergency contact numbers and response teams.
- **Resource Hub**: Offers articles, safety guidelines, and preparedness tips.
- **Volunteer Sign-Up**: Allows users to register as volunteers to assist in relief efforts.
- **Machine Learning Model**: Predicts high-risk earthquake zones based on historical data to improve preparedness and response planning.


## Machine Learning Model Details
- **Dataset**:
  - Contains 62 anonymized features related to earthquake data, including seismic activity, geological conditions, and historical impact.
  - Features include numerical and categorical variables, some requiring scaling and encoding.
    
- **Preprocessing**:
  - Identified and handled missing values using imputation techniques.
  - Scaled numerical features for consistency.
  - Performed feature engineering and selection to enhance model performance.
  - Split dataset into training and testing sets for evaluation.
    
- **Models Used**:
  - **Baseline Model**: Decision Tree (used as a benchmark for performance comparison).
  - **Optimized Model**: Random Forest (selected due to its high accuracy and ability to handle complex feature interactions).
  - **Comparison Model**: Multinomial Logistic Regression (evaluated for interpretability and efficiency).
    
- **Evaluation Metrics**:
  - **Accuracy**: Measures the overall correctness of the model.
  - **Precision & Recall**: Evaluate the model’s ability to correctly identify high-risk areas.
  - **F1-score**: Balances precision and recall for a comprehensive assessment.
  - **Confusion Matrix**: Analyzes false positives and false negatives to understand model performance better.
    
- **Results**:
  - **Random Forest Model** outperformed other models, achieving the highest accuracy and generalization capability.
  - **Logistic Regression** provided valuable interpretability but had lower predictive accuracy.
  - Future model improvements could include ensemble learning and deep learning approaches.


## Future Enhancements
- **Real-time Earthquake Alert System**: Integrate API-based live earthquake alerts.
- **Enhanced Model Performance**: Implement deep learning techniques to improve prediction accuracy.
- **Accessibility & Multilingual Support**: Ensure inclusivity for global users.
- **AI-Powered Chatbots**: Provide immediate disaster response assistance.
- **Expanded Dataset**: Incorporate real-time seismic data to refine ML predictions.


