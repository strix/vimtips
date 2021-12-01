+++
title = "reselecting text"
date = "2020-05-18"
+++
You can quickly reselect the last visual mode area selection with `gv`

I have this in my vimrc as well:

```vim
" Select text that was last pasted
nnoremap gp `[v`]
```
