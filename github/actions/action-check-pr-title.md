# GitHub Action Check PR Title

## Workflow

```yaml
---
name: Check PR Title

on:
  pull_request_target:
    types:
    - opened
    - edited
    - synchronize

jobs:
  check-pr-title:
    name: Check PR Title
    runs-on: ubuntu-latest
    steps:
    - uses: amannn/action-semantic-pull-request@v3.4.0
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
