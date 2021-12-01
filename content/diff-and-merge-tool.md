+++
title = "git diff and merge tool"
date = "2021-07-03"
+++
If I ever used something for my merge/diff tool for git I would use either meld or diff-so-fancy but doing it in vim seems awesome as well:

Vim can be used as a mergetool to handle git merge conflict.

First, setup Vim as a mergetool in your gitconfig. Then, during a merge conflict, run:

```
git mergetool
```

You can then use Vim to pick which change(s) to apply to the working copy.

[source](https://twitter.com/learnvim/status/1410968295004594190)

To setup Vim as a mergetool in my gitconfig, I added these in my `~/.gitconfig` (your gitconfig may be in a different location):

```
[core]
  editor = vim
[merge]
  tool = vimdiff
  conflictstyle = diff3
[difftool]
  prompt = false

```

Useful commands.

To get changes from local/base/remote:
- :diffget LOCAL
- :diffget BASE
- :diffget REMOTE

To go to next/prev changes:
- ]c
- [c

