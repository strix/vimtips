+++
title = "show/debug key mappings"
date = "2021-04-06"
+++
Use `:verbose map` to show where key mapping(s) are defined (see `:help map-verbose`). There are other variants as well that can be used with or without `verbose`:

`:nmap` for normal mode mappings
`:vmap` for visual mode mappings
`:imap` for insert mode mappings

To output the shortcuts, with where they were defined, to a text file do:

```vim
:redir! > vim_keys.txt
:silent verbose map
:redir END
```
