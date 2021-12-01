+++
title = "a guide to splits"
date = "2019-11-01"
+++
[vim splits a guide to doing exactly what you want](https://technotales.wordpress.com/2010/04/29/vim-splits-a-guide-to-doing-exactly-what-you-want/)

Some things to consider adding to my vimrc per that post:

```vim
" window
nmap <leader>swl :topleft  vnew<CR>
nmap <leader>swh :botright vnew<CR>
nmap <leader>swk :topleft  new<CR>
nmap <leader>swj :botright new<CR>
" buffer
nmap <leader>sl :leftabove  vnew<CR>
nmap <leader>sh :rightbelow vnew<CR>
nmap <leader>sk :leftabove  new<CR>
nmap <leader>sj :rightbelow new<CR>
```
