# GitHub

Common GitHub files and templates that can be re-used across repos

### Usage

Can reference the `./.github/workflows/` templates prefixed with `_` in actual repositories as:

```yml
jobs:
  pull-request:
    permissions:
      pull-requests: read
    uses: IBMS-Pty-Ltd/GitHub/.github/workflows/_dotnet_pull_request.yml@main
    with:
      dotnet-version: 8.0.x
    secrets:
      FEED_ACCESSTOKEN: ${{ secrets.FEED_ACCESSTOKEN }}
```