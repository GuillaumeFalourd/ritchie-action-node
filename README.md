# ritchie-actions-node

This Github action works for Ritchie CLI formulas implemented in **NODE**.

[![Action workflow](https://github.com/GuillaumeFalourd/ritchie-actions-node/actions/workflows/main.yml/badge.svg)](https://github.com/GuillaumeFalourd/ritchie-actions-node/actions/workflows/main.yml)

## Use case

```bash
name: Action workflow

on:
 push:
 workflow_dispatch:

jobs:
  action_job:
    runs-on: ubuntu-latest
    name: Ritchie Action
    steps:
    - name: Run Ritchie Action Command
      uses: GuillaumeFalourd/ritchie-actions-node@v1.0
      with:
        rit-repo-url: https://github.com/ZupIT/ritchie-formulas-demo
        rit-formula-command: rit demo coffee-node --rit_name=Dennis --rit_coffee_type=espresso --rit_delivery=false
```

**Where:**

- `rit-repo-url` is the Github formula repository url where the formula is located.
- `rit-formula-command` is the formula command (with input flags if needed) implemented in node.
