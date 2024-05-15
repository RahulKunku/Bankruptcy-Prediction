# Bankruptcy Prediction Project

## Overview

This project aims to apply data mining algorithms to predict if a firm will file for bankruptcy. The project is part of the MGMT 571 course, where students participate in a Kaggle competition to develop predictive models using various econometric measures.

## Project Goals and Objectives

### Goals
- Develop a predictive model that accurately forecasts bankruptcy using a provided dataset.
- Compare different modeling techniques and select the best-performing model.
- Present the findings and insights gained from the project.

### Objectives
- Implement multiple data mining algorithms using SAS Enterprise Miner.
- Evaluate the models based on performance metrics such as ROC, AUC, and accuracy.
- Fine-tune the models to improve prediction accuracy and reduce overfitting.

## Process and Methodology

### Data Import and Preprocessing
- **File Import**: The training data is imported into the system and the class variable is updated to a binary target variable.
- **Data Partition**: The data is partitioned into training and validation sets using a 75:25 split for the best model and a 60:40 split for the second-best model. This helps in developing and assessing predictive models without overfitting.
- **Preprocessing Steps**:
  - Filtering out data points 3 standard deviations away from the mean.
  - Rejecting variables with high kurtosis and skewness.
  - Oversampling to balance the dataset.

### Modeling Techniques
Multiple modeling techniques were employed and compared:
- **Gradient Boosting**
- **Neural Network**
  - Default training technique with 136 maximum iterations.
  - RProp training technique with 100 iterations.
- **Ensemble Methods**
  - Voting-based posterior probabilities.
- **Logistic Regression**
  - Stepwise, forward, and backward selection.
  - Polynomial and interaction terms.
- **Decision Tree**

### Model Comparison and Selection
- **Model Comparison**: All models were linked to a comparison node with Valid_ROC or Train_ASE as the selection criteria.
- **Scoring**: The test data was imported separately and scored using the final models.
- **Save Data**: The results from the scoring step were saved for further analysis.

## Best Results

### Best Model
- **Data Partition**: 75:25 split (Train:Validation)
- **Modeling Techniques**:
  - Gradient Boosting
  - Neural Network
  - Ensemble (of above two)
- **Results**: Achieved the highest Valid_ROC and good performance on the test data.

### Second Best Model
- **Data Partition**: 60:40 split (Train:Validation)
- **Modeling Techniques**:
  - Neural Network (RProp)
  - Gradient Boosting
  - Logistic Regression (Forward and Backward Selection, Polynomial)
  - Decision Tree
- **Results**: Performed well on the validation data but slightly lower ROC compared to the best model.

## Key Insights and Takeaways

- The combination of different modeling techniques, especially ensemble methods, provided the best results.
- Proper data preprocessing and partitioning are crucial to improve model performance and reduce overfitting.
- Balancing simplicity and complexity is key to developing effective predictive models.
- Continuous iteration and evaluation are necessary to fine-tune the models and achieve better accuracy.

## Conclusion

The project successfully developed a predictive model for bankruptcy using various data mining algorithms. The best model combined gradient boosting, neural networks, and ensemble methods, achieving high accuracy and robust performance. These results demonstrate the effectiveness of data mining techniques in predicting financial outcomes and provide valuable insights for further applications.

## Additional Notes
- Ensure all data fields are formatted correctly when uploading to databases for analysis.
- Regularly update data sources and analytical models to reflect current trends and consumer behavior.
