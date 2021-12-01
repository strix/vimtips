+++
title = "indentation"
date = "2018-11-06"
+++
Stolen from [this site](https://www.cs.oberlin.edu/~kuperman/help/vim/searching.html). Definitely worth a full read.

`<C-d>` and `<C-t>` indent back and forward in insert mode

The normal mode equivalent is `>>` and `<<`

I typically use `==` for auto indentation but this comes in handy when you want to be explicit or there isn't any autoindentation

Using the [detectindent](https://github.com/ciaranm/detectindent) plugin, indentation is automatically detect indent based on what is already in the file (expandtab, shiftwidth, tabstop settings)
```vim
:autocmd BufReadPost * :DetectIndent
```
