# Prompt Design

The current workflow constructs a prompt around two pieces of user input:

1. Programming language
2. Natural-language programming requirement

Conceptual prompt:

```text
human: Write <language> code for the following instruction:
<message>
Assistant:
```

## Why prompt structure matters

The model needs explicit instructions about the expected output. A clear prompt reduces ambiguity and makes downstream parsing easier.

## Recommended production prompt

```text
You are a code generation assistant.

Generate only valid source code.

Programming language:
{language}

Task:
{message}

Requirements:
- Do not include Markdown fences.
- Do not include explanations unless explicitly requested.
- Return complete executable code.
```

This is a future improvement rather than a claim about the exact current implementation.
