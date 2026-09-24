# Troubleshooting

## Problem: API returns success but output is wrong

A successful HTTP status only proves that the request reached the API and a response was returned.

Check:

```text
API Gateway
   ↓
Lambda logs
   ↓
Bedrock response
   ↓
S3 object
```

## Problem: S3 file exists but is tiny/empty

Inspect the exact string passed to `PutObject`.

Verify:

- Bedrock response parsing
- content encoding
- response body decoding
- output variable
- S3 `Body`

## Problem: Bedrock invocation fails

Check:

- model ID
- Bedrock model access
- IAM permission
- Bedrock region
- request schema
- Lambda runtime compatibility

## Problem: Lambda dependency import fails

Check the Lambda Layer:

```text
Layer ARN
Runtime compatibility
Architecture
Package directory structure
Layer version
```

## Problem: Region confusion

The development screenshots contain resources from more than one AWS region. Verify the final configuration before publishing the architecture as authoritative.
