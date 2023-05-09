# PanelPrinter

<!--
Replace all of the following strings with the current printer.
     panel Panel PanelPrinter DefaultPanel
-->

![PanelPrinter Example](https://raw.githubusercontent.com/pterm/pterm/master/_examples/panel/animation.svg)

<p align="center"><a href="https://github.com/gozelle/pterm/blob/master/_examples/panel/main.go" target="_blank">(Show source of demo)</a></p>

## Usage

### Basic usage

```go
// Declare panels in a two dimensional grid system.
panels := pterm.Panels{
    {{Data: "This is the first panel"}, {Data: pterm.DefaultHeader.Sprint("Hello, World!")}, {Data: "This\npanel\ncontains\nmultiple\nlines"}},
    {{Data: "This is another panel line"}, {Data: "This is the second panel\nwith a new line"}},
}

// Print panels.
_ = pterm.DefaultPanel.WithPanels(panels).Render()
```

### Options

> To make a copy with modified options you can use:
> `pterm.DefaultPanel.WithOptionName(option)`
>
> To change multiple options at once, you can chain the functions:
> `pterm.DefaultPanel.WithOptionName(option).WithOptionName2(option2)...`

> [!TIP]
> Click the options and types to show the documentation on _pkg.go.dev_

| Option                                                                                        | Type                                                               |
| --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| [BottomPadding](https://pkg.go.dev/github.com/gozelle/pterm#PanelPrinter.WithBottomPadding)     | int                                                                |
| [BoxPrinter](https://pkg.go.dev/github.com/gozelle/pterm#PanelPrinter.WithBoxPrinter)           | [BoxPrinter](https://pkg.go.dev/github.com/gozelle/pterm#BoxPrinter) |
| [Padding](https://pkg.go.dev/github.com/gozelle/pterm#PanelPrinter.WithPadding)                 | int                                                                |
| [Panels](https://pkg.go.dev/github.com/gozelle/pterm#PanelPrinter.WithPanels)                   | [Panels](https://pkg.go.dev/github.com/gozelle/pterm#Panels)         |
| [SameColumnWidth](https://pkg.go.dev/github.com/gozelle/pterm#PanelPrinter.WithSameColumnWidth) | ...bool                                                            |
| [Writer](https://pkg.go.dev/github.com/gozelle/pterm#PanelPrinter.WithWriter)                   | io.Writer                                                          |

### Output functions

> This printer implements the interface [`RenderablePrinter`](https://github.com/gozelle/pterm/blob/master/interface_renderable_printer.go)

| Function  | Description        |
| --------- | ------------------ |
| Render()  | Prints to Terminal |
| Srender() | Returns a string   |

## Related

- [Override default printers](docs/customizing/override-default-printer.md)
