# go-linebreak

## Installation
```bash
go get -u github.com/mghyo/go-linebreak
```

## Purpose
The purpose of this package is to allow text files to be split up in a platform-agnostic manner.
* On Windows the newline character is `"\r\n"`
* On linux/darwin the newline character is `"\n"`

I wanted a way to split strings wihtout platform specific code in my codebase.

## Usage

```go
package main

import (
	"fmt"
	"strings"

	"github.com/mghyo/go-linebreak"
)

func main() {
	var str string
	str = "asd\nfgh\njkl"
	lines := strings.Split(str, linebreak.Linebreak)

	for _, line := range lines {
		fmt.Println(line)
	}
}
```
