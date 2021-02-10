# Using Scanf to read stdin into variable

There are times when you are going to want to read stdin into a variable. One possible
way to do this is to use [`fmt.Scanf`](https://golang.org/pkg/fmt/#Scanf)

We pass `Scanf` the format as the first arg and a pointer to the
variable we want to update

```go
var valueFromStdin string

fmt.Scanf("%s\n", &valueFromStdin)
```
