# rjsa

A command to release JavaScript action

> ![CAUTION]
> I've developed this tool only for my JavaScript actions.
> I don't assume that others use this tool.

## Requirements

- gh
- git
- GNU sed
- GitHub Access Token (contents:write, actions:write)

## How To Install

Put `rjsa` into $PATH.

e.g.

```sh
cp rjsa $HOME/bin
chmod a+x $HOME/bin/rjsa
```

## Usage

- REF: `gh workflow run`'s `-ref` option
- WORKFLOW: `gh workflow run`'s workflow id
- VERSION: A release version
- PR Number: A pull request number for pre-release

```sh
[REF=<REF>] [WORKFLOW=release.yaml] rjsa [<VERSION>] [<PR Number>]
```

e.g.

Release a pre-release version v1.0.0-0:

```sh
REF=ci-foo rjsa v1.0.0-0 100
```

Release v1.1.0:

```sh
rjsa v1.1.0
```

## LICENSE

[MIT](LICENSE)
