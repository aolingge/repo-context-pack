# GitHub Actions

Run repo-context-pack on every pull request.

```yaml
name: repo-context-pack

on:
  pull_request:
  push:
    branches: [main]

jobs:
  check:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 20
      - run: npx github:aolingge/repo-context-pack --path fixtures/good.txt --min-score 80 --annotations
```

SARIF output:

```bash
npx github:aolingge/repo-context-pack --path fixtures/good.txt --sarif > results.sarif
```

Do not upload reports that contain private logs, tokens, cookies, or credentials unless they have been redacted.
