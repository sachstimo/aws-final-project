# Telco Customer Churn Analysis Project

## Business Overview

This project analyzes customer churn for a telecommunications company using a comprehensive dataset containing demographic information, service subscriptions, location details, and churn behavior. The insights derived from this analysis will help the business reduce customer attrition, improve retention strategies, and increase customer lifetime value.

## Project Objectives

- Identify key factors contributing to customer churn
- Develop predictive models to forecast at-risk customers
- Create actionable business recommendations for reducing churn
- Implement automated data processing and analysis workflow using AWS

## Dataset Description

The Telco Customer Churn dataset provides a comprehensive view of customer attributes, service usage, location data, and churn behavior. This expanded dataset serves as a valuable resource for understanding churn patterns, customer segmentation, and developing targeted marketing strategies.

The dataset is based on the [Telco customer churn dataset from Hugging Face](https://huggingface.co/datasets/aai510-group1/telco-customer-churn)

### Data Structure and Storage

The project maintains two synchronized data storage locations:

1. **Local Data Directory (`/DATA`)**
   - `churn_data_full.csv`: Complete dataset with all features
   - `df_for_sm.csv`: Processed dataset ready for SageMaker
   - `best_threshold.pkl`: Optimal classification threshold
   - `average_cltv.pkl`: Average Customer Lifetime Value reference
   - `best_threshold_new.pkl`: Updated classification threshold

2. **AWS S3 Bucket (`telco-churn-cp`)**
   - Mirrors the local data structure
   - Organized into train/validate/test splits
   - Stores model artifacts and predictions
   - Maintains version control of processed datasets

This dual-storage approach ensures:
- Consistent data access across local development and cloud deployment
- Seamless transition between offline analysis and SageMaker implementation
- Version control of processed datasets and model artifacts
- Efficient data pipeline management

### Business Value

This dataset enables several business-critical analyses:

- **Customer churn prediction:** Develop machine learning models to predict which customers are at risk of churning, leveraging the expanded features.
- **Customer segmentation:**  Identify different customer segments based on demographics, service usage, location, and churn behavior.
- **Targeted marketing campaigns:**  Develop targeted marketing campaigns to retain at-risk customers or attract new customers, tailoring campaigns based on the insights derived from the merged dataset.
- **Location-based analysis:** Analyze customer churn trends based on specific locations, cities, or zip codes, and identify potential regional differences.

## AWS Data Processing Workflow

Our analysis follows a robust data processing pipeline implemented on AWS:

1. **Section 1: Set up of Environment**
   - Configure AWS credentials and permissions
   - Set up S3 bucket (`telco-churn-cp`) for data storage
   - Initialize SageMaker session and execution role
   - Install required dependencies (boto3, sagemaker, pandas, numpy, scikit-learn)

2. **Section 2: Hyperparameter Tuning**
   - Implement XGBoost algorithm with automated tuning
   - Configure training instance (ml.m5.xlarge)
   - Set up cross-validation and performance metrics
   - Optimize model parameters for maximum ROC AUC
   - Achieve 89% model accuracy through iterative improvement

3. **Section 3: Deploying Endpoint for Model**
   - Deploy real-time prediction endpoint
   - Configure batch processing capabilities
   - Set up model monitoring and logging
   - Implement automated resource cleanup
   - Enable scalable inference with ml.m5.xlarge instances

4. **Evaluation and Storing Predictions**
   - Generate and store batch predictions
   - Calculate model performance metrics
   - Analyze feature importance
   - Track prediction confidence scores
   - Store results in S3 for downstream analysis

## Key Dataset Attributes

The dataset contains 49 columns representing various customer attributes including:

- **Customer Demographics:** Age, gender, marital status, dependents, etc.
- **Service Subscriptions:** Internet type, phone service, streaming services, etc.
- **Financial Metrics:** Monthly charges, total charges, CLTV (Customer Lifetime Value)
- **Behavioral Indicators:** Contract type, payment method, tenure
- **Churn Information:** Churn status, reason, score, and category

## Business Insights and Limitations

### Key Business Insights

The analysis of this dataset can reveal:
- High-risk customer segments requiring immediate retention efforts
- Service combinations with the highest churn rates
- Cost-effective intervention points in the customer lifecycle
- Geographical patterns in customer attrition

### Limitations and Considerations

When leveraging this dataset for business decisions, consider:
- **Simulated Data:** The dataset might be based on simulated data and should be validated against real customer behavior
- **Business Context:** Incorporate market trends and competitive analysis for comprehensive decision-making
- **Implementation Challenges:** Consider operational feasibility of recommended interventions

## Next Steps and Recommendations

1. **Implementation Strategy:**
   - Prioritize quick-win retention initiatives based on analysis
   - Establish key performance indicators to measure success
   - Develop A/B testing framework for retention strategies

2. **Data Enhancement:**
   - Incorporate customer feedback data
   - Add competitive market positioning information
   - Include promotional campaign effectiveness metrics

3. **Model Deployment:**
   - Implement real-time churn prediction scoring
   - Develop automated customer intervention system
   - Establish continuous model retraining pipeline
