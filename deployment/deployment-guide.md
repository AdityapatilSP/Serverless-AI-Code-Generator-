# Deployment Guide

## Prerequisites

- AWS account
- IAM permissions to create/configure the required services
- Bedrock model access enabled where required
- Python
- AWS CLI (optional)
- Postman (optional)

## Services

Create/configure:

```text
1. S3 bucket
2. Lambda function
3. Lambda dependency layer
4. IAM execution role
5. API Gateway HTTP API
6. POST /code-generation route
7. Lambda integration
8. CloudWatch logging
```

## Deployment validation

After deployment:

```text
POST API
  ↓
Lambda invoked?
  ↓
Bedrock invoked?
  ↓
Code generated?
  ↓
S3 object created?
  ↓
S3 object contains expected code?
```

The repository should be updated with the final model ID, regions, bucket name pattern, and exact IAM permissions once the deployment configuration is finalized.
