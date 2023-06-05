npx create-next-app@latest --example with-cypress with-cypress-app

crée un repos gitlab
github>action>runner

comme gitlab github va aller chercher les configurations des runner ici

crée `.github/workflows/learn-github-actions.yml`

git add ., git commit -m "", git push

```yaml
name: learn-github-actions
on: [push]
jobs:
  check-bats-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: '14'
      - run: npm install -g bats
      - run: bats -v
```

crée des jobs pour arriver jusqu'au build