# Project Summary: Predicting Term Deposit Subscription

Objective:
Develop a predictive model to determine whether clients will subscribe to a term deposit based on various client attributes and past marketing campaign interactions. This project explored three different machine learning models: Random Forest, XGBoost, and LightGBM (LGB).

Data Description:

	•	The dataset includes attributes such as age, job type, marital status, education, credit default status, average yearly balance, housing loan status, personal loan status, communication type, last contact day and month, contact duration, number of contacts during the campaign, days since the client was last contacted, previous contact count, and outcome of the previous campaign.
	•	Target Variable: Whether the client subscribed to a term deposit (‘yes’ or ‘no’).

Data Preprocessing:

	•	Cleaning and Encoding: Converted categorical variables to numerical using one-hot encoding. Mapped binary variables (‘yes’, ‘no’) to 1 and 0 respectively. Applied standard scaling to numerical features.
	•	Imbalance Handling: Addressed class imbalance through resampling techniques and by using algorithms robust to imbalance.

Model 1: Random Forest

	•	Hyperparameter Tuning: Used Grid Search CV to find the best hyperparameters.
	•	Performance: Achieved an accuracy of 88.48%. However, the model struggled with the positive class (term deposit subscription), showing poor precision, recall, and F1-score for this class.
	•	Key Metrics:
	•	Accuracy: 88.48%
	•	Precision (Class 1): 0.00
	•	Recall (Class 1): 0.00
	•	F1-Score (Class 1): 0.00

Model 2: XGBoost

	•	Hyperparameter Tuning: Applied Grid Search CV for optimization.
	•	Performance: Achieved an accuracy of 76.58%. Demonstrated better recall for the positive class, but precision and F1-score indicated room for improvement in reducing false positives.
	•	Key Metrics:
	•	Accuracy: 76.58%
	•	Precision (Class 1): 0.31
	•	Recall (Class 1): 0.85
	•	F1-Score (Class 1): 0.45

Model 3: LightGBM (LGB)

	•	Hyperparameter Tuning: Used Grid Search CV to identify optimal parameters.
	•	Performance: Achieved an accuracy of 89.38%. Displayed a balance between precision and recall for the positive class, making it more effective in predicting term deposit subscriptions than Random Forest and XGBoost.
	•	Key Metrics:
	•	Accuracy: 89.38%
	•	Precision (Class 1): 0.54
	•	Recall (Class 1): 0.49
	•	F1-Score (Class 1): 0.51

Conclusion:
Among the three models tested, LightGBM provided the best balance of precision and recall for predicting term deposit subscriptions. While the overall accuracy was high across all models, further tuning and additional techniques may be required to improve the model’s performance on the minority class (term deposit subscribers). The project highlights the importance of model selection and hyperparameter tuning in addressing class imbalance and achieving robust predictive performance.
