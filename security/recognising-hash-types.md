# How to recognise hash types

If you look at the hash, you can tell that:

- if the hash starts by `$1$`, MD5 is used;
- if the hash starts by `$2$` or $2a$, Blowfish is used;
- if the hash starts by `$5$`, SHA-256 is used;
- if the hash starts by `$6$`, SHA-512 is used.

[Source](https://pentesterlab.com/exercises/unix_16/course)
