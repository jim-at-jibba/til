# How to cherry pick commits

There are often situations where we need to hotfix a bug but need the bugfix on both the hotfix branch and also on the main branch.

You could obviously just copy the fix across but an easier, less error prone solution is to use `git cherry-pick`

Let’s say you’ve written some code in commit 62ecb3 of the feature branch that is very important right now.
It may contain a bug fix or code that other people need to have access to now. Whatever the reason,
you want to have commit 62ecb3 in the master branch right now, but not the other code you’ve written in the feature branch.

Here comes git cherry-pick. In this case, 62ecb3 is the cherry and you want to pick it!

```
git checkout master
git cherry-pick 62ecb3

```

[A good source](https://www.devroom.io/2010/06/10/cherry-picking-specific-commits-from-another-branch/)
