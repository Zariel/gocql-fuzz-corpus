go-fuzz corpus for [gocql](https://github.com/gocql/gocql)
===========

This is for protocol version 2 only so ensure that both the fuzz.go and frame_test.go are configured to run in protocol 2 mode.

Usage
====

Install [go-fuzz](https://github.com/dvyukov/go-fuzz)
`go get github.com/dvyukov/go-fuzz/...`

Complile gocql
`go-fuzz-build github.com/gocql/gocql`

Run some fuzz
`go-fuzz -bin=./gocql-fuzz -corpus=gocql-fuzz-corpus/corpus-v2 -workdir=fuzz-workdir`

Add test case to `frame_test.go`, fix bug and submit a PR!