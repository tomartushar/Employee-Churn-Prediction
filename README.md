# Employee Churn Prediction

Predict whether an employee will churn from the company or not, and analyze the factors responsible for, or having the most influence on, employee churn.

## Dataset

The dataset is available on [Kaggle](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv).

| Variable               | Description                                                                      |
|------------------------|----------------------------------------------------------------------------------|
| satisfaction_level     | Employee-reported job satisfaction level [0&ndash;1]                             |
| last_evaluation        | Score of employee's last performance review [0&ndash;1]                           |
| number_project         | Number of projects the employee contributes to                                   |
| average_monthly_hours | Average number of hours the employee worked per month                             |
| time_spend_company     | How long the employee has been with the company (years)                           |
| work_accident          | Whether or not the employee experienced an accident while at work                 |
| left                   | Whether or not the employee left the company                                      |
| promotion_last_5years  | Whether or not the employee was promoted in the last 5 years                      |
| department             | The employee's department                                                        |
| salary                 | The employee's salary (U.S. dollars)                                              |

## Results

| Model                         | Precision | Recall | F1-Score | Accuracy |
|-------------------------------|-----------|--------|----------|----------|
| Logistic Regression           | 0.75      | 0.81   | 0.77     | 0.81     |
| Naive Bayes                   | 0.87      | 0.80   | 0.82     | 0.80     |
| KNN                           | 0.79      | 0.88   | 0.83     | 0.94     |
| SVC                           | 0.80      | 0.88   | 0.84     | 0.94     |
| Decision Tree                 | 0.78      | 0.92   | 0.85     | 0.94     |
| Quadratic Discriminant Analysis | 0.90   | 0.85   | 0.86     | 0.85     |
| Random Forest                 | 0.87      | 0.90   | 0.88     | 0.96     |
| Gradient Boosting             | 0.92      | 0.87   | 0.89     | 0.97     |
| XGBoost                       | 0.91      | 0.89   | 0.90     | 0.97     |

## Conclusion

The XGBoost model achieves the best `F1-Score` and `Accuracy`. Features such as `last_evaluation`, `number_project`, `tenure`, and `overworked` are most important in deciding employee churn.

Insights:
* Employees involved in more than 4 projects have a higher chance of leaving the company.
* Most employees leave between the 2nd and 5th years of employment.
* A significant proportion of employees who leave are either overworked with good evaluation scores or underworked with low evaluation scores.
