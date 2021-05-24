# Git wont reflect case changes in files names unless explicitly told too.

If you change the case of a file name you need to explicitly tell Git that
you have made this change or it wont be reflected in your code and things will break!

`git mv -f [oldfile] [newfile]`