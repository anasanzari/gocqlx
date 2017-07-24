# gocqlx [![GoDoc](http://img.shields.io/badge/go-documentation-blue.svg?style=flat-square)](http://godoc.org/github.com/mmatczuk/gocqlx) [![Go Report Card](https://goreportcard.com/badge/github.com/mmatczuk/gocqlx)](https://goreportcard.com/report/github.com/mmatczuk/gocqlx) [![Build Status](http://img.shields.io/travis/mmatczuk/gocqlx.svg?style=flat-square)](https://travis-ci.org/mmatczuk/gocqlx)

Package `gocqlx` is a `gocql` extension, similar to what `sqlx` is to `database/sql`.

It provides a new type that seamlessly wraps `gocql.Iter` and provide
convenience methods which are useful in the development of database driven
applications.  None of the underlying gocql.Iter methods are changed.
Instead all extended behavior is implemented through new methods defined on
wrapper type.

The wrapper type enables you to bind iterator row into a struct. Under the
hood it uses `sqlx/reflectx` package, models / structs working whit `sqlx` will
also work with `gocqlx`.

## Installation

    go get github.com/mmatczuk/gocqlx

## Example

See [example test](https://github.com/mmatczuk/gocqlx/blob/master/example_test.go).