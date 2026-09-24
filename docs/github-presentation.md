# GitHub Presentation Guide

## Repository headline

**Serverless AI Code Generator — Natural Language to Cloud-Stored Source Code**

## One-line portfolio description

> A serverless Generative AI backend that accepts natural-language coding requirements through API Gateway, invokes a foundation model through Amazon Bedrock, and persists generated source code in Amazon S3.

## Resume-style bullets

- Built a serverless AI code-generation API using Amazon API Gateway, AWS Lambda and Amazon Bedrock.
- Designed a prompt-driven inference workflow that converts natural-language programming requirements into source code.
- Persisted generated code artifacts in Amazon S3 and used CloudWatch for execution-level observability.
- Integrated AWS SDK/Boto3 and a Lambda dependency layer for the runtime environment.
- Tested and debugged the complete API → Lambda → Bedrock → S3 workflow using Postman and CloudWatch.

## Architecture keywords

`AWS Lambda` `Amazon Bedrock` `API Gateway` `Amazon S3` `CloudWatch` `Boto3` `Generative AI` `Serverless` `Python` `IAM`

## Interview explanation

> "I built a serverless code-generation backend where API Gateway exposes an HTTP endpoint, Lambda handles request parsing and orchestration, Bedrock performs foundation-model inference, and S3 stores the generated source artifact. CloudWatch provides observability. I validated the complete request path using Postman and the AWS console."
