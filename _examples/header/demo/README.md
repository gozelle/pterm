# header/demo

![Animation](animation.svg)

```go
package main

import "github.com/gozelle/pterm"

func main() {
	// Print a default header.
	pterm.DefaultHeader.Println("This is the default header!")
	pterm.Println() // spacer
	pterm.DefaultHeader.WithFullWidth().Println("This is a full-width header.")
}

```
