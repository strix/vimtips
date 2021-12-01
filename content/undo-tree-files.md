+++
title = "undo tree files"
date = "2020-05-13"
+++
To save your undo trees in a separate file, use `:wundo` and `:rundo`.

Example:

After editing hello.txt, I can save my undo tree with

```vim
:wundo! hello.undo
```

Close vim. Open hello.txt. We can't undo. This is normal. Now read undo file:

```vim
:rundo hello.undo
```

You can undo now.

[source](https://twitter.com/learnvim/status/1257752345703841793?s=20)

