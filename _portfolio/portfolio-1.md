---
title: "Ames Housing Price Prediction"
excerpt: "Analyzed and predicted housing prices in the Ames dataset using different machine learning techniques.<br/>"
collection: portfolio
---

[https://github.com/wesleymeredith/Ames-Housing-Project/blob/main/README.md](https://github.com/wesleymeredith/Ames-Housing-Project/blob/main/README.md)

This study focused on predicting housing prices using the Ames Housing dataset, comparing four different machine learning approaches: Decision Tree, Random Forest, XGBoost, and Artificial Neural Networks (ANN). The project particularly investigated whether feature engineering or hyperparameter tuning had a greater impact on model performance.

## Dataset
- **Training Set**: 1,460 samples
- **Testing Set**: 1,459 samples
- **Features**: 79 property attributes (both numerical and categorical)
- **Target Variable**: Sale Price

## Methodology

### Data Preprocessing
Our preprocessing pipeline began with thorough missing value treatment. For categorical data, we imputed missing values with 'None', while numerical missing values were filled using mean or median values as appropriate. We then applied label encoding to convert categorical variables into a format suitable for our models.

### Feature Engineering
The feature engineering process involved creating several new meaningful features. We developed polynomial features for key metrics like square footage and room numbers, created interaction features combining variables like age and size, and generated ratio features such as living area to lot size ratio. These efforts significantly improved our model's predictive power, raising the average Mutual Information score from 0.126 to 0.162.

### Model Implementation
We implemented a comprehensive evaluation framework testing each model against various preprocessing techniques. Starting with baseline implementations, we explored PCA dimensionality reduction, feature selection, outlier removal, feature engineering, and hyperparameter tuning to understand their relative impact on model performance.

## Results

### Model Performance Comparison
Best RMSE scores for each model after feature engineering:
- Decision Tree: 32,542
- Random Forest: 27,590
- XGBoost: 26,598
- ANN: 21,776

### Key Insights
The feature engineering process proved to be the most impactful factor in improving model performance, reducing RMSE by approximately 15-30% across all models while enhancing interpretability. PCA, contrary to our initial expectations, showed poor improvements across all models. This was largely due because PCA conflicts with the non-linear relationships between the features in housing dataset.

Our ANN implementation saw significant improvements through architectural optimization. The three-layer design (128/64/32 neurons) with L2 Regularization and ReLU activation functions proved most effective.

Interestingly, hyperparameter tuning showed minimal impact compared to feature engineering, suggesting that model architecture and data quality were more crucial than parameter optimization for this particular problem.

## Final Thoughts/Future Work
This project was my first end-to-end data science project. There was a lot to uncover and learn from doing an entire project for the first time, like how important the cleaning and transformation of the data is.

If I were to come back to this project in the future, I would integrate maybe some ensembling approaches and emphasize a lot more importance on the EDA.

*This project was completed in collaboration with Kaijun Zhang and Yiran Zhu at North Carolina State University.*