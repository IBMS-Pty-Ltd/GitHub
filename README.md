# GitHub

Common GitHub files and templates that can be re-used across repos

### Usage

Reference the `./.github/workflows/` templates in actual repositories like:

```yml
jobs:
  pull-request:
    uses: IBMS-Pty-Ltd/GitHub/.github/workflows/dotnet_pull_request.yml@main
    with:
      dotnet-version: 8.0.x
      solution-path: 'MyProject.slnx'
    secrets:
      FEED_ACCESSTOKEN: ${{ secrets.FEED_ACCESSTOKEN }}
    # or "secrets: inherit"
```
