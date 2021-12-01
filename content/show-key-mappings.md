+++
title = "show/debug key mappings"
date = "2021-04-06"
+++
use `:verbose map` to show where key mapping(s) are defined (see `:help map-verbose`)

To output the shortcuts, with where they were defined, to a text file do:

```vim
:redir! > vim_keys.txt
:silent verbose map
:redir END
```
