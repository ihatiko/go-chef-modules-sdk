```bash
  go get github.com/ihatiko/go-chef-modules-sdk
```
```go
package main

import (
	"fmt"
	sdk "github.com/ihatiko/go-chef-modules-sdk"
	"github.com/spf13/cobra"
)

func main() {
	module := sdk.NewModule()
	module.AddCommands(
		module.NewCommand("sandbox test", func(cmd *cobra.Command, args []string) {
			fmt.Println("sandbox test")
		}),
	)
	module.Run()
}

```
