# install-dylan-tool

A GitHub Action to install
[dylan-tool](https://github.com/dylan-lang/dylan-tool). This action also
invokes the
[install-opendylan](https://github.com/dylan-lang/install-opendylan) Action.

To install the latest dylan-tool release:

```yaml
    - uses: dylan-lang/install-dylan-tool@v3
```

To install a specific released version:

```yaml
    - uses: dylan-lang/install-dylan-tool@v3
      with:
        tag: v0.12.0
```

`tag` must exactly match a tagged version in the [dylan-tool
repository](https://github.com/dylan-lang/dylan-tool).

When this Action has completed the `dylan` executable is available on the
`PATH` and the `dylan-tool` directory contains the `dylan-tool` checkout and
build products.

See the [hello](https://github.com/cgay/hello) repository for the canonical
example of using this Action.
