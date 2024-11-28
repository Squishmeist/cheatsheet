# Go

- [Go](https://go.dev/doc/): A general-purpose language.
- [Echo](https://echo.labstack.com/docs): A web framework for Go to handle HTTP requests.
- [Viper](https://github.com/spf13/viper): A configuration loading solution.

# Installation

1. **Install Go**: Follow the instructions on the [official Go website](https://golang.org/doc/install) to install Go.

   ```sh
   snap install go --classic
   export PATH=$PATH:/usr/local/go/bin
   ```

2. **Install Air**: Air is a live reloading tool for Go applications. Install it by running:

   ```sh
   go install github.com/air-verse/air@latest
   export PATH=$PATH:$(go env GOPATH)/bin
   ```

# Commands

## Setup

New project:

```sh
go mod init <project-name>
```

Remove all downloaded modules:

```sh
go clean -modcache
```

## Testing

To run tests, use the following command:

```sh
go test ./...
```

For more detailed output, use the `-v` flag:

```sh
go test -v ./...
```

### Gotestsum

To have formatted test outputs, install [gotestsum](https://github.com/gotestyourself/gotestsum):

```sh
go install gotest.tools/gotestsum@latest
```

To run tests and generate a coverage report:

```sh
gotestsum -- -coverprofile=cover.out ./...
```

To view test results grouped by file:

```sh
gotestsum --format testname
```

For more options and detailed usage, refer to the [gotestsum documentation](https://github.com/gotestyourself/gotestsum).
