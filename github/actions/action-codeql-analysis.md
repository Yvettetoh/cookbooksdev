# GitHub Actions CodeQL Analysis

## Links

- [Actions Cache](https://github.com/actions/cache/blob/main/examples.md#php---composer)
- [Code Repository](https://github.com/github/codeql)
- [Main Website](https://codeql.github.com/)

## Workflow

**Refer:** `./.github/workflows/codeql-analysis.yml`

```yaml
---
name: CodeQL

on:
  push:
    branches:
    - main
  pull_request:
    branches:
    - main
  schedule:
  - cron: 0 0 * * *  # https://crontab.guru/#0_0_*_*_*

jobs:
  analyze:
    name: Analyze
    runs-on: ubuntu-18.04
    permissions:
      actions: read
      contents: read
      security-events: write

    strategy:
      fail-fast: false
      matrix:
        language:
        - javascript

    steps:
    - name: Checkout code
      uses: actions/checkout@v2
      with:
        # Disabling shallow clone is recommended for improving relevancy of reporting
        fetch-depth: 0

    - name: Initialize CodeQL
      uses: github/codeql-action/init@v1
      with:
        languages: ${{ matrix.language }}

    - name: Autobuild
      uses: github/codeql-action/autobuild@v1

    - name: Perform CodeQL Analysis
      uses: github/codeql-action/analyze@v1
```
