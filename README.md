# End-to-End Churn Prediction using AWS SageMaker

This project builds an end-to-end customer churn prediction model using AWS SageMaker.
The goal is to predict whether a customer will be retained (`retained = 1`) or churn (`retained = 0`)
based on behavioral, transactional, and engagement features.

## Project Structure
- `data_wrangler_partial_execution/`
  - Data exploration, cleaning, and feature engineering using SageMaker Data Wrangler
- `sagemaker_studio_model_evaluation/`
  - Model training, deployment, and evaluation using SageMaker built-in XGBoost

## Key Steps
1. Data exploration and feature engineering using SageMaker Data Wrangler
2. Feature pipeline export (partial execution due to AWS service quota limitations)
3. Model training using SageMaker built-in XGBoost
4. Model deployment as a real-time SageMaker endpoint
5. Model evaluation using AUC ROC metric
6. Cleanup of deployed resources

## Results
- Model: SageMaker built-in XGBoost (binary classification)
- Evaluation Metric: AUC ROC
- AUC ROC from endpoint predictions: 0.9843756474134537

## Notes on AWS Limitations
Exporting the Data Wrangler pipeline to SageMaker Feature Store via a Processing job
was partially completed due to AWS account-level service quota restrictions.
To ensure full project completion, feature engineering was replicated using pandas
prior to model training.

## Cleanup
All deployed SageMaker endpoints were deleted after testing to avoid ongoing charges.
