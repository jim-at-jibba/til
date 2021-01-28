# Check if a string only contains letters

To check if a string only contains letters, use the following:

```go
package main

import "fmt"
import "unicode"

func IsLetter(s string) bool {
    for _, r := range s {
        if !unicode.IsLetter(r) {
            return false
        }
    }
    return true
}
func main() {
    fmt.Println(IsLetter("Alex")) // true
    fmt.Println(IsLetter("123"))  // false
}
```
