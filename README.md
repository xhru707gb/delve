# Delve

A fork of [go-delve/delve](https://github.com/go-delve/delve) — the Go debugger.

[![Build Status](https://api.cirrus-ci.com/github/your-org/delve.svg)](https://cirrus-ci.com/github/your-org/delve)

## Overview

Delve is a debugger for the Go programming language. This fork maintains compatibility with the upstream project while introducing additional features and fixes.

## Installation

### From source

```bash
git clone https://github.com/your-org/delve.git
cd delve
go install ./cmd/dlv
```

### Using `go install`

```bash
go install github.com/your-org/delve/cmd/dlv@latest
```

### Pre-built binaries

Pre-built binaries are available on the [releases page](https://github.com/your-org/delve/releases).

## Usage

### Debug a package

```bash
dlv debug github.com/your/package
```

### Attach to a running process

```bash
dlv attach <pid>
```

### Connect to a headless debug server

```bash
dlv connect localhost:2345
```

### Run tests with debugger

```bash
dlv test github.com/your/package
```

## Documentation

Full documentation is available at the [upstream project](https://github.com/go-delve/delve/tree/master/Documentation).

## Differences from upstream

This fork tracks upstream closely. Notable differences:

- Additional CI configurations for extended platform support
- Windows ARM64 test workflow
- Custom release pipeline via GoReleaser

## Building

Requirements:
- Go 1.21 or later
- For Linux: `apt-get install -y golang gcc`
- For macOS: Xcode command line tools

```bash
make build
```

## Contributing

Please read the [contribution guidelines](CONTRIBUTING.md) before submitting a pull request.

When filing issues, use the provided [issue template](.github/ISSUE_TEMPLATE/issue_template.yml).

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

Upstream project copyright © 2014-present go-delve contributors.
