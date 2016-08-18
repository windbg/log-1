[![GoDoc](https://godoc.org/github.com/cybozu-go/log?status.svg)][godoc]
[![Build Status](https://travis-ci.org/cybozu-go/log.svg?branch=master)](https://travis-ci.org/cybozu-go/log)
[![Go Report Card](https://goreportcard.com/badge/github.com/cybozu-go/log)](https://goreportcard.com/report/github.com/cybozu-go/log)
[![License](https://img.shields.io/github/license/cybozu-go/log.svg?maxAge=2592000)](LICENSE)

Logging framework for Go
========================

This is a logging framework mainly for our Go products.

Be warned that this is a _framework_ rather than a library.
Most features cannot be configured.

Features
--------

* Light-weight.

    Hard-coded maximum log buffer size and 1-pass formatters
    help cybozu/log be memory- and CPU- efficient.

* Built-in logfmt and JSON Lines formatters.

    By default, logs are formatted in syslog-like plain text.
    [logfmt][] and [JSON Lines][jsonl] formatters can be used alternatively.

* Automatic redirect for Go standard logs.

    The framework automatically redirects [Go standard logs][golog]
    to itself.

* Reopen handler.

    The framework comes with a handy writer that reopens the log file
    upon signal reception.  Useful for work with log rotating programs.

    Only for non-Windows systems.

Usage
-----

Read [the documentation][godoc].

License
-------

[MIT](https://opensource.org/licenses/MIT)

[logfmt]: https://brandur.org/logfmt
[jsonl]: http://jsonlines.org/
[golog]: https://golang.org/pkg/log/
[godoc]: https://godoc.org/github.com/cybozu-go/log
