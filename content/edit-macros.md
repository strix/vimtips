+++
title = "editing macros"
date = "2020-11-03"
+++
If you need to edit a macro (because you forgot to remember to add a motion key for the macro to be effectively repeatable):

1. `:let @q="` open the `q` register
2. `<C-r><C-r>q` paste the contents of the q register into the buffer
3. ^ add the missing motion to return to the front of the line
4. " add a closing quote
5. <Enter> finish editing the macro

An alternate way of doing this is:

1. `"qp` paste the contents of the register to the current cursor position
2. `I` enter insert mode at the beginning of the pasted line
3. ^" add the missing motion to return to the front of the line and add a quote
4. <Escape> return to normal mode
5. `"qyy` yank this new modified macro back into the `q` register
6. `dd` delete the pasted register from the file your editing

_(Use `ctrl+v <key>` to get the actual character key for escape sequences for macros and whatever else)_
