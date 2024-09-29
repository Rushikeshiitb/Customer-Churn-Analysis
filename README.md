# Churn Data Analysis Project

## Overview
This project focuses on analyzing customer churn in a telecommunications dataset. It involves exploratory data analysis (EDA) and the development of predictive models to classify customer churn effectively.

## Files
- **EDA Code**: Contains the code for data exploration and visualization.
- **Prediction Model Code**: Includes the code for developing and evaluating predictive models.

## Data Exploration and Insights
- The dataset contains 7,043 customers with 21 features.
- A significant imbalance was observed in the target variable, with fewer churned customers compared to non-churned ones.
- Key factors influencing churn include:
  - **High churn rates**: Month-to-month contracts, lack of online security, lack of tech support, and being in the first year of subscription.
  - **Lower churn rates**: Long-term contracts, subscriptions without internet services, and customers engaged for over five years.
- Gender, availability of phone service, and the number of multiple lines showed minimal impact on churn rates.

## Data Cleaning and Preparation
- Data cleaning involved handling missing values and converting categorical variables into dummy variables for model training.
- Feature engineering, such as binning tenure, helped in analyzing churn based on customer tenure effectively.

## Model Development
- A Decision Tree Classifier was initially used to predict churn, yielding low accuracy due to the imbalanced nature of the dataset.
- The SMOTEENN technique was applied to oversample the minority class (churned customers) and enhance model performance.
- A Random Forest Classifier was implemented, showing improved accuracy and recall for the churned customers compared to the Decision Tree.

## Performance Evaluation
- Models were evaluated using precision, recall, F1 score, and accuracy. The Random Forest model with SMOTEENN demonstrated the best results, achieving an accuracy of approximately 92%.
- Further experiments with PCA showed that while dimensionality reduction can be beneficial, it did not yield better results compared to the Random Forest model.

## Model Deployment
- The final model (Random Forest Classifier with SMOTEENN) was saved using pickle, making it ready for deployment in a production environment where it can be accessed through APIs for real-time predictions.

## Future Work
- Explore additional classifiers to enhance model performance.
- Incorporate more features, such as customer engagement metrics, for deeper insights into churn.
- Implement a continuous monitoring system for the model's performance in production to ensure effectiveness over time.

## Conclusion
This analysis lays a solid foundation for understanding customer churn and developing effective retention strategies for telecommunications companies.
