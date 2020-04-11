# hCaptcha

[![build status](https://img.shields.io/travis/kataras/hcaptcha/master.svg?style=for-the-badge&logo=travis)](https://travis-ci.org/kataras/hcaptcha) [![report card](https://img.shields.io/badge/report%20card-a%2B-ff3333.svg?style=for-the-badge)](https://goreportcard.com/report/github.com/kataras/hcaptcha) [![godocs](https://img.shields.io/badge/go-%20docs-488AC7.svg?style=for-the-badge)](https://godoc.org/github.com/kataras/hcaptcha)

Lightweight [hCaptcha](https://www.hcaptcha.com/) middleware for the Go Programming Language.

## Installation

The only requirement is the [Go Programming Language](https://golang.org/dl).

```sh
$ go get -u github.com/kataras/hcaptcha
```

## Getting Started

First of all, navigate to <https://www.hcaptcha.com/>, create an account and attach a [new site](https://dashboard.hcaptcha.com/sites) for [development](https://docs.hcaptcha.com/#localdev).

Import the package:

```go
package main

import "github.com/kataras/hcaptcha"
```

Create a new client:

```go
client := hcaptcha.New(your_secret_key)
```

Wrap a page's handler:

```go
humanHandler := client.Handler(handler)
```

For a complete example please navigate through [_examples](_examples) directory.

## License

This software is licensed under the [MIT License](LICENSE).