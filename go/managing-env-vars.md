# Managing env variables

In any application you are likely to use need to store and access environment variables.

The most straight forward way to get started is to use the dotenv package

`go get github.com/joho/godotenv`

```go
// Load the .env file in the current directory
godotenv.Load()

// or

godotenv.Load(".env")

```

Example

```go
package main

import (

    ...
  "github.com/joho/godotenv"
)


// use godot package to load/read the .env file and
// return the value of the key
func goDotEnvVariable(key string) string {

  // load .env file
  err := godotenv.Load(".env")

  if err != nil {
    log.Fatalf("Error loading .env file")
  }

  return os.Getenv(key)
}

func main() {
    // os package
    ...

  // godotenv package
  dotenv := goDotEnvVariable("STRONGEST_AVENGER")

  fmt.Printf("godotenv : %s = %s \n", "STRONGEST_AVENGER", dotenv)
}
```

For more complex needs [Viper](https://github.com/spf13/viper) may be worth looking at.

[source](https://towardsdatascience.com/use-environment-variable-in-your-next-golang-project-39e17c3aaa66)
