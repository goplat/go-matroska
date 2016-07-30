# Golang Matroska and WebM Container Format Implementation

[![Build Status](https://travis-ci.org/pixelbender/go-matroska.svg)](https://travis-ci.org/pixelbender/go-matroska)
[![Coverage Status](https://coveralls.io/repos/github/pixelbender/go-matroska/badge.svg?branch=master)](https://coveralls.io/github/pixelbender/go-matroska?branch=master)
[![Go Report Card](https://goreportcard.com/badge/github.com/pixelbender/go-matroska)](https://goreportcard.com/report/github.com/pixelbender/go-matroska)
[![GoDoc](https://godoc.org/github.com/pixelbender/go-matroska?status.svg)](https://godoc.org/github.com/pixelbender/go-matroska)

## Installation

```sh
go get github.com/pixelbender/go-matroska
```

## Usage

```go
import "github.com/pixelbender/go-matroska/matroska"
import "os"

func main() {
    reader, err := os.Open("example.mkv")
    // Handle filesystem errors
    defer reader.Close()
    
    file := new(matroska.File)
    dec := NewDecoder(reader)
    err = dec.Decode(file)
    
    // Handle decoding errors
}

```

## Specifications

- [ ] [Matroska Media Container - Specifications](https://matroska.org/technical/specs/index.html)
- [ ] [WebM Container - Guidelines](https://www.webmproject.org/docs/container/)
