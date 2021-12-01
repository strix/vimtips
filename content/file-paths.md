+++
title = "current file paths"
date = "2020-01-24"
+++
In insert mode, type `<C-r>%` to insert the name of the current file.

In command mode (after typing a colon), type `<C-r>%` to insert the name of the current file. The inserted name can then be edited to create a similar name.

In normal mode, type `"%p` to put the name of the current file after the cursor (or `"%P` to insert the name before the cursor).

`1ctrl+g` - print the full file path of a file in vim.

Plain `ctrl+g` will do the relative path, `1` will do full path, `2` will do full path and buffer number.

Some handy keymaps:

```vim
" Copy relative file path to system clipboard
nnoremap <leader>cf :let @+=expand("%")<CR>
" Copy absolute file path to system clipboard
nnoremap <leader>cF :let @+=expand("%:p")<CR>
" Copy file name to system clipboard
nnoremap <leader>ct :let @+=expand("%:t")<CR>
" Copy directory name to system clipboard
nnoremap <leader>ch :let @+=expand("%:p:h")<CR>
```
