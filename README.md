Example:

```
package main

import (
    "github.com/esenti/godraw"
)

func main() {
    context := godraw.CreateContext(800, 600)

    for !context.Window.ShouldClose() {
        context.Clear(godraw.Color{1.0, 1.0, 0.0})
        context.DrawRectangle(100, 300, 20, 20, godraw.Color{0.5, 0.4, 0.2})
        context.DrawRectangle(200, 200, 345, 12, godraw.Color{0.5, 0.7, 0.2})
        context.DrawRectangle(399, 312, 345, 124, godraw.Color{0.1, 0.9, 0.1})

        context.Window.SwapBuffers()
        context.PollEvents()
    }

}
```
