# Find a file that contains a specific string in the name

Sometimes you want to search for a file that has a certain string in
its name.

Use `find`:

`find . -maxdepth 1 -name "*string*" -print`

It will find all files in the current directory (delete maxdepth 1 if you want it recursive) containing "string" and will print it on the screen.

If you want to avoid file containing ':', you can type:

`find . -maxdepth 1 -name "*string*" ! -name "*:*" -print`

If you want to use grep (but I think it's not necessary as far as you don't want to check file content) you can use:

`ls | grep touch`

But, I repeat, find is a better and cleaner solution for your task.

[Source](https://stackoverflow.com/questions/11328988/find-all-files-with-name-containing-string)
