# `lerna publish`: "Current HEAD is already released" while actual package is not released to npm

Sometimes if you have run `lerna publish` and it has failed you will get the following error:

> lerna publish: "Current HEAD is already released" while actual package is not released to npm

This sucks, it should be transactional.

To solve this you can publish using the package and not git as the source of truth:

`lerna publish from-package`

[Source](https://github.com/lerna/lerna/issues/1709)
