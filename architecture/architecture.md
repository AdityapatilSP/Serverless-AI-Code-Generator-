# Architecture

## High-level architecture

```mermaid
flowchart TB
    Client["Client / Postman"]
    API["Amazon API Gateway<br/>POST /code-generation"]
    Lambda["AWS Lambda<br/>bedrock_code_generation"]
    Bedrock["Amazon Bedrock"]
    S3["Amazon S3<br/>code-output/"]
    CW["Amazon CloudWatch"]
    Layer["Lambda Layer<br/>boto3 / dependencies"]

    Client --> API
    API --> Lambda
    Lambda --> Bedrock
    Bedrock --> Lambda
    Lambda --> S3
    Lambda --> CW
    Lambda -.-> Layer
```

## Design principle

The architecture separates concerns:

- **API Gateway** handles HTTP exposure.
- **Lambda** orchestrates application logic.
- **Bedrock** performs generative AI inference.
- **S3** persists generated artifacts.
- **CloudWatch** provides observability.
- **IAM** controls service-to-service permissions.

This means the project does not need a permanently running backend server.
