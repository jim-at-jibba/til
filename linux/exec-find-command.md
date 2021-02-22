# Execute a command from the results of a `find`

Sometimes you want to execute a command from the result of a `find` command.

- `find / -name file.txt -exec cat {} \;`
- `{}` is a placeholder for path returned from find
