# GitHub Action: install-with-retry

GitHub action that retries installing dependencies for less CI flakiness.

## Usage

```yml
steps:
    - uses: Doist/action-install-with-retry@main
      with:
          install-cypress: 0
          skip-install-husky: 1
          gh-packages-token: ${{ secrets.GH_PACKAGES_TOKEN }}
```

> We're aware of the irony that one input is `install-cypress` while the other is `skip-install-husky`. For simplicity's sake we kept the naming the tools provide. PRs to change this are welcome.

## Publish

To publish a new version you need to create a tag and push it (or create it on GitHub):

```sh
git tag -f -a v2.2.0 -m "Version 2.2.0"
```
