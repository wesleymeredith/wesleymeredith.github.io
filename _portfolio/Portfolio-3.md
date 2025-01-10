---
title: "Drowsiness Detector"
excerpt: "Detecting drowsiness based on EAR values via OpenCV.<br/>"
collection: portfolio
---

[https://github.com/wesleymeredith/Drowsiness-Detection](https://github.com/wesleymeredith/Drowsiness-Detection)

In this project, I collaborated with a team to develop and compare multiple machine learning approaches for housing price prediction using the Ames Housing dataset. We implemented and evaluated four distinct models: Decision Trees, Random Forest, XGBoost, and Artificial Neural Networks (ANN).

Key aspects of the project included:
- Comprehensive data preprocessing and feature engineering
- Implementation of multiple ML architectures
- Comparative analysis of model performance
- Investigation of feature engineering impact versus hyperparameter tuning

The project demonstrated that feature engineering had a more significant impact on model performance than hyperparameter tuning, with our best model achieving a Root Mean Square Error (RMSE) of 21,776 on the test set.

Detailed results and analysis are available below.

# Housing Price Prediction Project - Results Summary

## Project Overview
This study focused on predicting housing prices using the Ames Housing dataset, comparing four different machine learning approaches: Decision Tree, Random Forest, XGBoost, and Artificial Neural Networks (ANN). The project particularly investigated whether feature engineering or hyperparameter tuning had a greater impact on model performance.

## Dataset
- **Training Set**: 1,460 samples
- **Testing Set**: 1,459 samples
- **Features**: 79 property attributes (both numerical and categorical)
- **Target Variable**: Sale Price

## Methodology

### Data Preprocessing
1. **Missing Value Treatment**
   - Categorical data: Imputed with 'None'
   - Numerical data: Imputed using mean/median values
   - Label encoding for categorical variables

2. **Feature Engineering Highlights**
   - Created polynomial features (square footage, room numbers)
   - Developed interaction features (age × size)
   - Generated ratio features (living area to lot size)
   - Improved average Mutual Information score from 0.126 to 0.162

### Model Implementation
Each model was evaluated using various preprocessing techniques:
- Baseline implementation
- PCA dimensionality reduction
- Feature selection
- Outlier removal
- Feature engineering
- Hyperparameter tuning

## Key Findings

### Model Performance Comparison
Best RMSE scores for each model after feature engineering:
- Decision Tree: 32,542
- Random Forest: 27,590
- XGBoost: 26,598
- ANN: 21,776

### Critical Insights
1. **Feature Engineering Impact**
   - Most significant improvement across all models
   - Reduced RMSE by approximately 15-30%
   - Enhanced model interpretability

2. **PCA Effectiveness**
   - Showed poor performance across models
   - Conflicted with non-linear nature of the data
   - Reduced model interpretability

3. **ANN Optimization**
   - Three-layer architecture (128/64/32 neurons) outperformed two-layer design
   - L2 Regularization significantly improved performance
   - ReLU activation function proved most effective

4. **Hyperparameter Tuning**
   - Showed minimal impact compared to feature engineering
   - Limited by dataset complexity
   - Suggested diminishing returns in model optimization

## Conclusions

1. **Feature Engineering Superiority**
   - Proved more valuable than hyperparameter tuning
   - Successfully captured complex relationships in the data
   - Enhanced model performance across all architectures

2. **Model Performance**
   - ANN with L2 Regularization achieved best performance
   - XGBoost showed strong performance with lower computational requirements
   - Simpler models (Decision Trees) provided valuable baseline metrics

3. **Practical Applications**
   - Results suggest focusing resources on feature engineering over parameter optimization
   - Demonstrated importance of domain knowledge in feature creation
   - Highlighted value of ensemble and neural network approaches for complex predictions

## Future Directions
1. Exploration of K-nearest neighbor algorithms
2. Integration of broader real estate domain knowledge
3. Investigation of automated feature generation techniques
4. Development of hybrid modeling approaches

*This project was completed in collaboration with Kaijun Zhang and Yiran Zhu at North Carolina State University.*