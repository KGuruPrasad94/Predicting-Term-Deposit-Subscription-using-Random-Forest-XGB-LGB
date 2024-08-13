# Predicting Term Deposit Subscription

## Objective
The goal of this project is to develop a predictive model to determine whether clients will subscribe to a term deposit based on various client attributes and past marketing campaign interactions. This project explores three different machine learning models: Random Forest, XGBoost, and LightGBM (LGB).

## Data Description
The dataset includes a variety of attributes related to the clients and their interaction with past marketing campaigns:
- **Client Attributes**: Age, job type, marital status, education, credit default status, average yearly balance, housing loan status, personal loan status.
- **Campaign Attributes**: Communication type, last contact day and month, contact duration, number of contacts during the campaign, days since the client was last contacted, previous contact count, and the outcome of the previous campaign.
- **Target Variable**: Whether the client subscribed to a term deposit (`yes` or `no`).

## Data Preprocessing
- **Cleaning and Encoding**: Categorical variables were converted to numerical values using one-hot encoding. Binary variables (`yes`, `no`) were mapped to 1 and 0, respectively. Standard scaling was applied to numerical features.
- **Imbalance Handling**: Class imbalance was addressed using resampling techniques and by employing algorithms robust to imbalance.

## Model 1: Random Forest
- **Hyperparameter Tuning**: Grid Search CV was used to optimize hyperparameters.
- **Performance**: Achieved an accuracy of 88.48%. However, the model struggled with the positive class (term deposit subscription), showing poor precision, recall, and F1-score for this class.
- **Key Metrics**:
  - Accuracy: 88.48%
  - Precision (Class 1): 0.00
  - Recall (Class 1): 0.00
  - F1-Score (Class 1): 0.00

## Model 2: XGBoost
- **Hyperparameter Tuning**: Grid Search CV was applied for optimization.
- **Performance**: Achieved an accuracy of 76.58%. Demonstrated better recall for the positive class, but precision and F1-score indicated room for improvement in reducing false positives.
- **Key Metrics**:
  - Accuracy: 76.58%
  - Precision (Class 1): 0.31
  - Recall (Class 1): 0.85
  - F1-Score (Class 1): 0.45

## Model 3: LightGBM (LGB)
- **Hyperparameter Tuning**: Grid Search CV was used to identify optimal parameters.
- **Performance**: Achieved an accuracy of 89.38%. Displayed a balance between precision and recall for the positive class, making it more effective in predicting term deposit subscriptions than Random Forest and XGBoost.
- **Key Metrics**:
  - Accuracy: 89.38%
  - Precision (Class 1): 0.54
  - Recall (Class 1): 0.49
  - F1-Score (Class 1): 0.51

## Conclusion
Among the three models tested, **LightGBM** provided the best balance of precision and recall for predicting term deposit subscriptions. While the overall accuracy was high across all models, further tuning and additional techniques may be required to improve the model’s performance on the minority class (term deposit subscribers). This project underscores the importance of model selection and hyperparameter tuning in addressing class imbalance and achieving robust predictive performance.

## Future Enhancements
- **Further Hyperparameter Tuning**: Explore more advanced techniques for hyperparameter optimization.
- **Ensemble Methods**: Combine models to leverage the strengths of each approach.
- **Data Augmentation**: Generate synthetic data to address class imbalance more effectively.
- **Feature Engineering**: Explore additional features that might improve model performance.

---
