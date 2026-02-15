---
on:
  schedule: daily
  workflow_dispatch:

permissions:
  contents: read
  issues: read
  pull-requests: read

safe-outputs:
  create-issue:
    title-prefix: "[daily-status] "
    labels: [report, daily-status]
    close-older-issues: true
---

# Daily Repository Status Report

Create a concise daily status report for the xhs-demo repository as a GitHub issue.

## What to include

- Recent commits and what changed (last 24h)
- Open pull requests and their status
- Open issues summary
- Code quality observations (any patterns, improvements spotted)
- Actionable next steps for maintainers

## Style

- Keep it concise and scannable
- Use bullet points
- Highlight anything that needs attention
- Include links to relevant PRs/issues/commits
- End with 2-3 suggested improvements or experiments
