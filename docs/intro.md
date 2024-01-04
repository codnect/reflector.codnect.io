---
slug: /
sidebar_position: 1
---

# Introduction

Let's discover **Reflector in less than 5 minutes**.

## What is Reflector?

**Reflector** is a reflection library written in Go, which provides an abstraction for built-in reflection API in GoLang. Unlike the built-in reflection API, it is easy to use and understand.

## What you'll need

- [Golang](https://go.dev/dl/) version 1.18 or above.

Run the following Go command to install the Reflector package:

```bash
go get -u codnect.io/reflector
```


## Usage

There are two main functions provided by Reflector to be able to get the type of any instance.
    
* **reflector.TypeOf**: get the type without any instance
* **reflector.TypeOfAny**: get the type of any instance

Here's an example of how to use Reflector:

```go
package main

import (
    "codnect.io/reflector"
)

type MyCustomType struct {
	
}

func main() {
	// get the type without any instance
	rType := reflector.TypeOf[MyCustomType]()
	
	// get the type of any instance
	rType = reflector.TypeOfAny(MyCustomType{})
}
```