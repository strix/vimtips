+++
title = "edit previously committed files"
date = "2022-01-25"
+++
print a list of files that were modified in a given commit (from `git log` or from GitHub)

```
:read !git show --pretty="format:" --name-only <commit-hash>
```

or for the files modified in the latest commit

```
:read !git show --pretty="format:" --name-only HEAD
```

and then use `gf` to open those files.

It was useful when I needed to ssh into a machine and open the same files that I had last modified in the commit to make further changes.
