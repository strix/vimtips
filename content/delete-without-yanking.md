+++
title = "delete without yanking"
date = "2021-04-06"
+++
```vim
" delete without yanking
nnoremap <leader>d "_d
vnoremap <leader>d "_d

" replace currently selected text with default register without yanking it
vnoremap <leader>p "_dP
```

`_` is the "blackhole register"
