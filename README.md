# :construction: setup-distrobuilder (WIP)
## :rotating_light: CAREFUL! WORKING IN PROGRESS!

Install [distrobuilder](https://linuxcontainers.org/distrobuilder/introduction/) in GitHub Actions

## Usage

```yml
---
name: setup-distrobuilder

on:
  # Allows manual workflow run (must in default branch to work)
  workflow_dispatch:
  push:
  pull_request:

jobs:
  setup-distrobuilder:
    runs-on: ubuntu-22.04
    steps:

    - name: Setup Distrobuilder
      uses: supertemaki/setup-distrobuilder@main
      with:
        channel: latest/stable
```

## Inputs

### `channel`

- version of distrobuilder.
- available version list is [snapcraft](https://snapcraft.io/distrobuilder).
- default: `latest/stable`
