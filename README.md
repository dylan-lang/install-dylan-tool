# install-dylan-tool

A GitHub Action to install
[dylan-tool](https://github.com/dylan-lang/dylan-tool). This action also
invokes the
[install-opendylan](https://github.com/dylan-lang/install-opendylan) Action.

To install the latest dylan-tool release:

```yaml
    - uses: dylan-lang/install-dylan-tool@v1
```

To install a specific released version:

```yaml
    - uses: dylan-lang/install-dylan-tool@v1
      with:
        tag: v4.2.1
```

`tag` must exactly match a tagged version in the [dylan-tool
repository](https://github.com/dylan-lang/dylan-tool).

**Important:** This Action must be used **after**
[actions/checkout@v2](https://github.com/actions/checkout) when using the
default `path:` (i.e., the current directory) because `actions/checkout@v2`
deletes everything in the repo directory first.

When this Action has completed, three artifacts exist in the current directory:

1.  A symbolic link to the `dylan` executable.

2.  A symbolic link to the `dylan-compiler` executable.

3.  A symbolic link named `opendylan` that points to the Open Dylan
    installation directory.

See the [hello](https://github.com/cgay/hello) repository for the canonical
example of using this Action.
