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

### Business Value

This dataset enables several business-critical analyses:

- **Customer churn prediction:** Develop machine learning models to predict which customers are at risk of churning, leveraging the expanded features.
- **Customer segmentation:**  Identify different customer segments based on demographics, service usage, location, and churn behavior.
- **Targeted marketing campaigns:**  Develop targeted marketing campaigns to retain at-risk customers or attract new customers, tailoring campaigns based on the insights derived from the merged dataset.
- **Location-based analysis:** Analyze customer churn trends based on specific locations, cities, or zip codes, and identify potential regional differences.

## AWS Data Processing Workflow

Our analysis follows a robust data processing pipeline implemented on AWS:

1. **Data Ingestion**
   - Raw data stored in Amazon S3 buckets
   - Automated data uploads using AWS Transfer Family

2. **Data Processing**
   - ETL jobs using AWS Glue for data transformation
   - Data quality checks and validation using AWS Lambda functions

3. **Data Storage and Management**
   - Processed data stored in Amazon RDS (PostgreSQL)
   - Data catalog maintained using AWS Glue Data Catalog

4. **Analysis and Modeling**
   - Machine learning models developed using Amazon SageMaker
   - SQL queries for data exploration via Amazon Athena

5. **Visualization and Reporting**
   - Interactive dashboards created with Amazon QuickSight
   - Automated report generation and distribution

6. **Orchestration**
   - Workflow orchestration using AWS Step Functions
   - Scheduling with Amazon EventBridge

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
- **Simulated Data:** The dataset is based on simulated data and should be validated against real customer behavior
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

## Technical Documentation

For detailed technical documentation on the AWS implementation, data processing scripts, and machine learning models, please refer to the project's technical documentation in the `/docs` directory.