# Model Training, Deployment, and Evaluation

This folder contains the notebook used to train, deploy, and evaluate
the churn prediction model using AWS SageMaker.

## Model
- Algorithm: SageMaker built-in XGBoost
- Task: Binary classification (customer churn)

## Steps Performed
1. Load and preprocess dataset
2. Feature engineering (replicating Data Wrangler logic)
3. Train-test split
4. Model training using SageMaker XGBoost
5. Deployment as a real-time SageMaker endpoint
6. Endpoint invocation using `predictor.predict()`
7. Evaluation using AUC ROC metric

## Evaluation Result
- AUC ROC (endpoint predictions): 0.9844

## Deployment
The model was deployed as a SageMaker real-time endpoint and successfully
invoked via API calls. The endpoint was deleted after evaluation to
avoid ongoing AWS charges.
