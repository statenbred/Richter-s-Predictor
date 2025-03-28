# Rebuilding Nepal

## **Project Goal**
This project aimed to develop a model that predicts a building's structural integrity based on its damage classification.

## **Backstory**
On April 25th, 2015, Nepal was struck by an earthquake with a 7.8 magnitude, impacting four different countries: Nepal, China, Bangladesh, and India. The earthquake claimed the lives of thousands, left over half a million people homeless, triggered landslides, and caused an avalanche that wound up claiming the lives of 200 people. 

## **Impact by Numbers**
- **People affected**: 8 million people were impacted by the earthquake.
- **Death and injured toll**: Nearly 9000 dead and 22,000 people injured.
- **Displacement numbers**: More than 600,000 people were displaced due to their homes being destroyed.
- **Damage Assessment**: $7.1 billion in damages across four countries.
- **Rebuilding Costs**: Estimated $10 billion across all four countries

## **Project Steps**

- **EDA**:
  - Contains 62 anonymized features related to earthquake data, including seismic activity, geological conditions, and historical impact.
  - Features include numerical and categorical variables, some requiring scaling and encoding.
  - Geographic location, damage grade, building structure types, building structure attributes, potential correlating features
    
- **Preprocessing**:
  - Identified and handled missing values using imputation techniques.
  - Scaled numerical features for consistency.
  - Performed feature engineering and selection to enhance model performance.
  - Split the dataset into training and testing sets for evaluation.
    
- **Models Used**:
  - **Baseline Model**: Random Forest (used as a benchmark for performance comparison).
  - **Optimized Model**: Catboost Classifier (selected due to its high accuracy and ability to handle complex feature interactions).
    
- **Evaluation Metrics**:
  - **Accuracy**: Random Forest - 66% baseline model and 71% refined model (massive overfitting). Catboost Classifier - 70% baseline model and 71% optimized model (no overfitting and very stable)
  - **Precision & Recall**: Random Forest - .66 precision and .69 recall. Catboost Classifier - .71 precision and .61 recall (no overfitting).
  - **F1-score**: Random Forest .66 and Catboost Classifier .71.
  - **Confusion Matrix**: Both models identified Class 2 most accurately, misclassified Class 3 as Class 2 (nearly 6000 instances), and struggled to identify Class 1
    
- **Results**:
  - **Random Forest Model**: while the test accuracy was nearly identical to Catboost, the model wasn't very stable. The instability of the model alongside its inability to identify Classes 1 and 3 forced me to try a different model. 
  - **Catboost Classifier**: stable model with more upside than Random Forest. More efficient model of the two, no pipeline or encoding needed to fit the model. Catboost Classifier has target encoding built into it. Learning rate showed the model made genuine predictions based on what it learned. Highest accuracy .714
  - **Error Analysis**: identified which features the model relies heavily on, and the grouping of features that are causing the model to make erroneous predictions. With some more feature engineering and hyperparameter tuning, we can increase the model's ability to predict a building's structural integrity based on its damage classification.

## **Recommendations**: 
- **Model Investment**: use error analysis findings to target features that are causing misclassification, feature engineering, and tune hyperparameters.
- **Structural Recommendations**:
    - Prioritize retrofitting high-risk structures with reinforced concrete or concrete mortar brick
    - Phase out mud mortar stone construction, especially in high-risk regions
    - Use cement mortar brick for cost-effectiveness
    - Implement structural assessment programs targeting mud, mud mortar stone buildings
        - retrofit where possible
        - propose cement mortar brick as replacements where retrofitting is not possible


