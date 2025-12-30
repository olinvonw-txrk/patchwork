# pipeline-scheduler-serverless

A lightweight solution enabling scheduled pipeline execution for CI/CD free tiers.  

Implementation overview:

1. An AWS Lambda function named `pipeline-scheduler` is deployed
2. The `pipeline-scheduler` Lambda function executes hourly
3. Each execution triggers the CI/CD REST API to initiate a build

Prerequisites:

1. Install https://serverless.com/ on your local machine
2. Configure AWS account with API credentials for serverless.com (reference: https://serverless.com/framework/docs/providers/aws/guide/credentials/)

Deployment steps:

1. Update the handler.js constants with your CI/CD API key, project identifier, etc.
2. Execute `serverless deploy`
3. Verify pipeline execution initiated successfully on your CI/CD dashboard
