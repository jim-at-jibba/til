# Executing a command as a different user with find

If you have find as a sudo command for another user, you
are able to execute commands as that user, even if the sudo
user does not have these permissions.

In the example below. Your user has permission to use find
with sudo for the victim user. With this we can use the `-exec`
command to read the contents of files that we find with `find`

- `sudo -u victim /usr/bin/find / -name key.txt -exec cat {} \;`
- `{}` is a placeholder for path returned from find
