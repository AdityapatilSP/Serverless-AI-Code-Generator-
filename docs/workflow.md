# Complete Workflow

## 1. Client request

The developer sends:

```json
{
  "key": "python",
  "message": "implement binary search"
}
```

## 2. API Gateway

API Gateway receives:

```text
POST /code-generation
```

and forwards the request to Lambda.

## 3. Lambda

Lambda parses the request and extracts the language and task.

## 4. Prompt construction

The values are inserted into the prompt sent to the model.

## 5. Bedrock

Bedrock performs inference using the configured foundation model.

## 6. Response processing

Lambda extracts the generated code from the Bedrock response.

## 7. S3

The generated source is written into:

```text
code-output/
```

## 8. Response

The API returns an HTTP response to the client.

## 9. Observability

Lambda execution information is available in CloudWatch.

---

## Engineering insight

The key architectural boundary is:

```text
AI inference ≠ artifact persistence
```

Bedrock generates the content, while S3 owns the durable artifact.

That separation allows the application to evolve independently on both sides.
