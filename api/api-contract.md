# API Contract

## Route

```http
POST /code-generation
```

## Request

```json
{
  "key": "python",
  "message": "implement binary search"
}
```

### Fields

| Field | Meaning |
|---|---|
| `key` | Requested programming language |
| `message` | Natural-language coding requirement |

## Response observed during testing

```json
"code generation complete"
```

The API can later be upgraded to return structured metadata, for example:

```json
{
  "status": "success",
  "language": "python",
  "s3_key": "code-output/binary_search.py"
}
```

## Validation recommendations

A production API should validate:

- request body exists
- JSON is valid
- language is supported
- message is non-empty
- message length is within an allowed limit
