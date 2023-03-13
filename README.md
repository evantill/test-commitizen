# test-commitizen
:construction: test repository

# Commitizen bootstrap

see https://github.com/googleapis/release-please/blob/main/docs/cli.md for bootstraping

see https://github.com/google-github-actions/release-please-action for action installation

```bash
cat <<EOF > .github/workflows/draft-release-please.yml
on:
  push:
    branches:
      - main

permissions:
  contents: write
  pull-requests: write

name: release-please

jobs:
  release-please:
    runs-on: ubuntu-latest
    steps:
      - uses: google-github-actions/release-please-action@v3
        with:
          release-type: node
          package-name: release-please-action
EOF
```