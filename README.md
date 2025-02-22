# setup-gopass

This action installs and configures [Gopass](https://github.com/gopasspw/gopass) and, optionally, the [Summon Gopass Provider](https://github.com/gopasspw/gopass-summon-provider).

## Example Usage

```yml
name: Setup Gopass
on: [push, pull_request]
jobs:
  setup-gopass:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Setup Gopass
        uses: mauhlik/setup-gopass@v1
```

## Available Options

- version: Specifies the version of Gopass to install. Defaults to the latest stable version.
- install-provider: Boolean to indicate whether to install the Gopass Summon Provider. Defaults to 'false'.
- provider-version: Optionally specify the version of the Gopass Summon Provider.
- download-url: The download url where to download gopass binary
- provider-download-url: The download url where to download gopass summon provider binary 

