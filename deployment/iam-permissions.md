# IAM Permissions

The Lambda execution role should follow least privilege.

Conceptually, it requires permissions for:

```text
CloudWatch Logs
    ├── CreateLogGroup
    ├── CreateLogStream
    └── PutLogEvents

Amazon Bedrock
    └── Model invocation

Amazon S3
    └── PutObject on the required output prefix
```

Avoid:

```text
Action: "*"
Resource: "*"
```

when narrower permissions can be used.

Never commit IAM access keys or secret credentials to GitHub.
