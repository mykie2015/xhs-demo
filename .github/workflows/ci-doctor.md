---
on:
  issues:
    types: [opened, reopened]

permissions:
  contents: read
  issues: read

safe-outputs:
  add-comment:
    max: 1
  add-labels:
---

# Bug Triage Assistant

When a new issue is opened, analyze it and provide initial triage.

## Steps

1. Read the issue title and description
2. Search the codebase for related files and code patterns
3. Identify potential root causes based on the error description
4. Check recent commits for related changes that might have introduced the bug
5. Add a comment with your analysis including:
   - Likely affected files
   - Potential root cause
   - Suggested fix approach
   - Severity assessment (critical/high/medium/low)
6. Add appropriate labels (e.g., bug, priority, component area)

## Guidelines

- Be specific about file paths and line numbers when possible
- Reference relevant commits if the bug seems related to recent changes
- Keep the analysis concise but actionable
