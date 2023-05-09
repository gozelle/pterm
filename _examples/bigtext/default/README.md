# bigtext/default

![Animation](animation.svg)

```go
package main

import (
	"github.com/gozelle/pterm"
	"github.com/gozelle/pterm/putils"
)

func main() {
	pterm.DefaultBigText.WithLetters(putils.LettersFromString("PTerm")).Render()
}

```
