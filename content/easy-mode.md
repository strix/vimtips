+++
title = "easy mode"
date = "2022-01-10"
+++
vim has an easy mode. You enable it by using the `-y` (`vim -y`). It makes vim behave like a regular "click-and-type" text editor. In this mode, regular shortcuts work as expected, `ctrl + s` for save, `ctrl + c` for copy, `ctrl + v` paste, `ctrl + z` to undo, `ctrl + y` redo.

The downside (and the reason nobody makes a big deal about it) is that is was designed to be used inside a GUI, so there is no shortcut to quit. You need to close whatever graphical interface vim is in.

Not all is lost, I think it provides a nice base to use vim for quick edits. For the people who will never use vim on purpose, I will recommend creating a `.vimrc` on their home folder with this content.

```vim
" Enable 'easy mode'
source $VIMRUNTIME/evim.vim

"  Ctrl + q to Quit vim
inoremap <c-q> <c-o>:q<cr>
```

This will create a `ctrl + q` shortcut to quit. You could also replace (or add) `<Esc>` as a shortcut to quit.

This way even if you enter vim by accident it will behave somewhat like a "normal" text editor.

[source](https://dev.to/vonheikemen/comment/1d966)
