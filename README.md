# install-dylan-tool

GitHub Action to install dylan-tool. This action invokes the
https://github.com/dylan-lang/install-opendylan action.

This action can be invoked as follows:

```yaml
jobs:
  your-job:
    runs-on: ubuntu-latest
    steps:
      - uses: dylan-lang/install-dylan-tool@v1
      - ...more steps...
```

If a specific version of
[`dylan-tool`](https://github.com/dylan-lang/dylan-tool) is required it can be
passed in like this:

```yaml
jobs:
  your-job:
    runs-on: ubuntu-latest
    steps:
      - uses: dylan-lang/install-dylan-tool@v1
        with:
          version: v4.2.1
      - ...more steps...
```
