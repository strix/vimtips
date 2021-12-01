+++
title = "relative copy and paste"
date = "2020-08-17"
+++
Relative copy and paste in vim:

[https://ptc-it.de/relative-copy-paste-in-vim/](https://ptc-it.de/relative-copy-paste-in-vim/)

## tl;dr

`:t` is an alias for `:co[py]` and can be used in command mode like so

`:-12t.<cr>`

This will copy 12 lines above the cursor and paste on the current line it also works with different destinations (`:-12t+19<cr>`) and [ranges](https://vimhelp.org/usr_10.txt.html#10.3)

`:3t9` - copy line 3 to line 9. Reads 3 to 9.

`:3t.` - copy line 3 to the current line.
