# Actions Node.js

## Workflow

```yaml
name: GitHub Actions Workflow with NPM cache

on: [push]

jobs:
  build:
    runs-on: ubuntu-18.04

    steps:
    - name: Checkout code
      uses: actions/checkout@v2
      with:
        # Disabling shallow clone is recommended for improving relevancy of reporting
        fetch-depth: 0

    - uses: actions/setup-node@v1
      with:
        node-version: 14.2.0

    - name: Cache NPM dependencies
      uses: actions/cache@v1
      with:
        path: ~/.npm
        key: ${{ runner.OS }}-npm-cache-${{ hashFiles('**/package-lock.json') }}
        restore-keys: |
          ${{ runner.OS }}-npm-cache-

    - name: Install NPM dependencies
      run: npm install
```
