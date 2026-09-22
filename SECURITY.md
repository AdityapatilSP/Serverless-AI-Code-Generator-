# Security Notes

Before making this repository public:

- Never commit AWS access keys or secret keys.
- Never commit `.env` files containing credentials.
- Do not expose unnecessary AWS account IDs in screenshots.
- Use least-privilege IAM policies.
- Restrict S3 permissions to the required bucket/prefix.
- Protect the API with an authorization mechanism for production use.
- Avoid logging secrets, tokens, or sensitive user input.
- Validate and sanitize generated filenames before writing to S3.
- Treat generated code as untrusted content until it has been validated.

This project is a learning/portfolio implementation and should be hardened before production use.
