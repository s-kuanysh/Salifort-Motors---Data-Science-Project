# Capstone Project: Providing Data-Driven Suggestions for HR at Salifort Motors

## Project Overview
This project aims to support the HR department at Salifort Motors in understanding and improving employee satisfaction and retention. The company collected data from its employees and seeks to identify factors influencing employee turnover. By analyzing this dataset, the project intends to provide actionable insights and predictive modeling to help the HR team address the main question: What factors are likely to make an employee leave the company?

## Project Objectives
- **Data Analysis**: Analyze the dataset provided by the HR department to uncover patterns and relationships between employee attributes and turnover.
- **Predictive Modeling**: Build a machine learning model to predict whether an employee will leave the company.
- **Insights and Recommendations**: Identify key factors contributing to employee turnover and provide data-driven suggestions to improve employee retention.

## Dataset Description
The dataset consists of 14,999 rows and 10 columns, containing the following variables:

| Variable                | Description                                             |
|-------------------------|---------------------------------------------------------|
| satisfaction_level      | Employee-reported job satisfaction level [0–1]          |
| last_evaluation         | Score of employee's last performance review [0–1]       |
| number_project          | Number of projects the employee contributes to          |
| average_monthly_hours   | Average number of hours worked per month                |
| time_spend_company      | Number of years the employee has been with the company  |
| Work_accident           | Whether the employee experienced a work-related accident|
| left                    | Whether the employee left the company (0 = No, 1 = Yes) |
| promotion_last_5years   | Whether the employee was promoted in the last 5 years   |
| Department              | The employee's department                               |
| salary                  | The employee's salary (categorical: low, medium, high)  |

## Project Workflow
### 1. **Data Loading and Initial Inspection**
   - **Task**: Load the dataset and inspect its structure.
   - **Method**: The dataset was imported using Pandas, and an initial inspection was conducted to understand the features, including their types and presence of missing values.
   - **Outcome**: Provided a clear overview of the dataset, including basic statistics and data types.

### 2. **Exploratory Data Analysis (EDA)**
   - **Task**: Explore the dataset to identify trends, correlations, and patterns related to employee turnover.
   - **Method**:
     - **Visualizations**: Generated histograms, bar charts, and box plots to visualize distributions of key variables like satisfaction level, average monthly hours, and department.
     - **Correlation Analysis**: Used correlation matrices to identify relationships between features, such as satisfaction level and the likelihood of leaving the company.
   - **Outcome**:
     - Discovered patterns such as higher turnover among employees with low satisfaction levels or those working excessive hours.
     - Identified key factors that might influence an employee's decision to leave the company.

### 3. **Data Preprocessing**
   - **Task**: Prepare the dataset for predictive modeling.
   - **Method**:
     - **Encoding Categorical Variables**: Transformed categorical variables (e.g., department, salary) into numerical format using techniques like One-Hot Encoding.
     - **Feature Scaling**: Applied scaling to numerical features to ensure they are on the same scale, aiding model convergence.
   - **Outcome**: Produced a preprocessed dataset suitable for machine learning models, ensuring that features were correctly formatted and scaled.

### 4. **Predictive Modeling**
   - **Task**: Build machine learning models to predict employee turnover.
   - **Method**:
     - **Logistic Regression**: Implemented to classify the likelihood of an employee leaving the company.
     - **Random Forest Classifier**: Used to capture complex interactions between features and improve prediction accuracy.
     - **XGBoost Classifier**: Employed gradient boosting for robust and efficient predictions.
     - **Hyperparameter Tuning**: Utilized Grid Search (`GridSearchCV`) to find the best parameters for the models.
   - **Outcome**: Developed and compared multiple models, identifying the one with the highest predictive accuracy for employee turnover.

### 5. **Model Evaluation**
   - **Task**: Assess the performance of the predictive models.
   - **Method**:
     - **Confusion Matrix**: Visualized true positives, false positives, true negatives, and false negatives for classification tasks.
     - **Evaluation Metrics**: Calculated metrics like accuracy, precision, recall, and F1-score to evaluate model performance.
   - **Outcome**:
     - Identified the best-performing model for predicting employee turnover.
     - Highlighted the model's strengths and limitations in identifying employees at risk of leaving.

### 6. **Insights and Recommendations**
   - **Task**: Extract actionable insights from the analysis and modeling results.
   - **Method**:
     - **Feature Importance**: Analyzed the importance of features in the predictive model to understand key factors contributing to employee turnover.
     - **Pattern Recognition**: Recognized patterns indicating high turnover risk, such as low satisfaction levels or lack of promotion.
   - **Outcome**:
     - Provided insights into the primary drivers of employee turnover, such as job satisfaction, workload, and career development opportunities.
     - Recommended strategies for HR to improve employee retention, including enhancing job satisfaction and providing career advancement opportunities.

## Key Findings
- **Job Satisfaction**: Employees with low satisfaction levels are more likely to leave, indicating the need for initiatives to improve job satisfaction.
- **Work-Life Balance**: High average monthly working hours are associated with higher turnover, suggesting the importance of promoting work-life balance.
- **Career Advancement**: Lack of promotion opportunities is linked to higher turnover, emphasizing the need for clear career progression paths.
