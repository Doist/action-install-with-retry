# GitHub Action: install-with-retry

GitHub action that retries installing dependencies for less CI flakiness.

## Usage

```yml
steps:
    - uses: Doist/action-install-with-retry@main
      with:
          install-cypress: 0
          skip-install-husky: 1
```

> We're aware of the irony that one input is `install-cypress` while the other is `skip-install-husky`. For simplicity's sake we kept the naming the tools provide. PRs to change this are welcome.
