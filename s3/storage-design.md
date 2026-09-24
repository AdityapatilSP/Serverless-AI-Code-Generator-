# S3 Storage Design

Generated source files are stored beneath:

```text
code-output/
```

Example observed object:

```text
code-output/1100%.py
```

## Recommended production key

A safer naming strategy would be:

```text
code-output/{timestamp}-{safe_name}.{extension}
```

Example:

```text
code-output/2026-09-22T163037-binary-search.py
```

## Recommended metadata

Store:

- language
- model ID
- creation timestamp
- request ID
- original task
- generated filename

Avoid storing secrets or unnecessary personal information in object metadata.
