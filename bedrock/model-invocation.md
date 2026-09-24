# Model Invocation

The Lambda uses the AWS SDK for Python (**Boto3**) to communicate with the Bedrock Runtime API.

Conceptual sequence:

```text
Lambda
  ↓
Create Bedrock Runtime client
  ↓
Construct model request
  ↓
Invoke configured model
  ↓
Receive model response
  ↓
Decode response
  ↓
Extract generated text
```

The exact request schema is model-dependent. The final implementation should keep the model ID and model-specific request body configurable rather than hard-coded throughout the application.
