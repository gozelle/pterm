# interactive_continue/demo

![Animation](animation.svg)

```go
package main

import (
	"github.com/gozelle/pterm"
)

func main() {
	result, _ := pterm.DefaultInteractiveContinue.Show()
	pterm.Println() // Blank line
	pterm.Info.Printfln("You answered: %s", result)
}

```
