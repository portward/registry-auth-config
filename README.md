# Registry auth configuration

[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/portward/registry-auth-config/ci.yaml?style=flat-square)](https://github.com/portward/registry-auth-config/actions/workflows/ci.yaml)
[![go.dev reference](https://img.shields.io/badge/go.dev-reference-007d9c?logo=go&logoColor=white&style=flat-square)](https://pkg.go.dev/mod/github.com/portward/registry-auth-config)
[![built with nix](https://img.shields.io/badge/builtwith-nix-7d81f7?style=flat-square)](https://builtwithnix.org)

**Configuration library for building your own registry authorization service.**

> [!WARNING]
> **Project is under development. Backwards compatibility is not guaranteed.**

## Installation

```shell
go get github.com/portward/registry-auth-config
```

## Usage

This project is a _library_ that you can use to build your own authorization service for a container registry.

To see it in action, check out [https://github.com/portward/portward](https://github.com/portward/portward).

## Development

**For an optimal developer experience, it is recommended to install [Nix](https://nixos.org/download.html) and [direnv](https://direnv.net/docs/installation.html).**

Run tests:

```shell
go test -race -v ./...
```

Run linter:

```shell
golangci-lint run
```

To test changes made in [registry-auth](https://github.com/portward/registry-auth):

Make sure [registry-auth](https://github.com/portward/registry-auth) is checked out in the same directory:

```shell
cd ..
git clone git@github.com:portward/registry-auth.git
cd registry-auth-config
```

Set up a Go workspace:

```shell
go work init
go work use .
go work use ../registry-auth
go work sync
```

## License

The project is licensed under the [MIT License](LICENSE).
