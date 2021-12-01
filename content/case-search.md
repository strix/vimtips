+++
title = "case search"
date = "2017-10-04"
+++
Add `set ic` (`set ignorecase`) to your vimrc to have search ignore case by default.

Use case sensitive search only if a capital letter is used in the search
`set smartcase`

Set them in the editor temporarily in command mode:
`:set ic` or `:set smartcase`

To turn them off use
`:set noic` or `:set nosmartcase`

Toggling the settings could be useful as well with
`:set ic!` and query its value with `set ic?`
