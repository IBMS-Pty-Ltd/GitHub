# GitHub

Common GitHub files and templates that can be re-used across repos

### Usage

Reference the `./.github/workflows/` templates prefixed in actual repositories like:

```yml
permissions:
  contents: read

jobs:
  pull-request:
    # permissions:
    #   contents: read
    uses: IBMS-Pty-Ltd/GitHub/.github/workflows/dotnet_pull_request.yml@main
    with:
      dotnet-version: 8.0.x
    secrets:
      FEED_ACCESSTOKEN: ${{ secrets.FEED_ACCESSTOKEN }}
```