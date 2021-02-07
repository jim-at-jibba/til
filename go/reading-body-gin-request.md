# Reading the body of a Gin REST request

There are times when you just want to print out the body of a post request.

In the Gin framework you get passed the requests context which contains this information.

```go
func testFunc(c *gin.Context) {
    body, err := ioutil.ReadAll(c.Request.Body)
    if err != nil {
      log.Fatal(err)
    }

    println(string(body))
}
```

[Source](https://stackoverflow.com/a/59173430)
