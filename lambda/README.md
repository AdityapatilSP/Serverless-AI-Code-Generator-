# Lambda Implementation

The repository's screenshots document the deployed Lambda workflow, but the complete source code was not included in the supplied project evidence.

Replace `lambda_function.py` with the exact deployed function before presenting the repository as source-complete.

The documented contract is:

```text
API Gateway
    ↓
Lambda
    ↓
Bedrock Runtime
    ↓
Generated code
    ↓
S3 PutObject
    ↓
HTTP response
```

Do not invent model-specific response parsing or request fields when replacing the placeholder; copy them from the deployed implementation.
