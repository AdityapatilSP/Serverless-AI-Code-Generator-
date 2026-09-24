# CloudWatch Monitoring

Lambda writes execution logs to:

```text
/aws/lambda/bedrock_code_generation
```

## Useful log points

For debugging, log safe operational information such as:

```text
Request received
Language: python
Bedrock invocation started
Bedrock invocation completed
Generated code length: <N>
S3 upload started
S3 upload completed
```

Do **not** log credentials, tokens, sensitive prompts, or private user data unnecessarily.

## Debugging order

When a request fails:

1. Check API Gateway response.
2. Open the Lambda log stream.
3. Find the first exception.
4. Determine whether failure occurred before or after Bedrock.
5. Verify IAM permissions.
6. Verify the S3 upload.
7. Verify the S3 object contents.
