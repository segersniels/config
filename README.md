# config

Easy and user friendly config management for CLI applications.

## Usage

```go
package main

import (
  "github.com/segersniels/config"
)

type Config struct {
	Bar string `json:"bar"`
}

var CONFIG = config.NewConfig("foo", Config{
	Bar: "bar",
})

CONFIG.Bar = "baz"
err := CONFIG.Save()
if err != nil {
  panic(err)
}
```
