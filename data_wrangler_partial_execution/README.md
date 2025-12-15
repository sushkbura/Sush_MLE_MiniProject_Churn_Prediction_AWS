# Data Wrangler – Partial Execution

This folder contains the SageMaker Data Wrangler workflow used for:
- Data exploration
- Data cleaning
- Feature engineering

## Contents
- `data_wrangler_tea_churn.flow`: Data Wrangler flow file
- `data_wrangler_tea_churn.ipynb`: Exported Data Wrangler notebook
- `executed_data_wrangler_tea_churn.ipynb`: Partially executed Data Wrangler notebook

## Status
The Data Wrangler pipeline was successfully created and exported.
However, execution of the pipeline to SageMaker Feature Store using
a Processing job could not be fully completed due to AWS service quota
limitations on processing instance types.

## Features Engineered
- Customer tenure
- Time to first order
- Recency
- Subscription score
- Digital engagement indicators
- Purchase intensity
- One-hot encoding of categorical variables

These same features were recreated using pandas for downstream model training.
