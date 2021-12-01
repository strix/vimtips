+++
title = "persistent folds"
date = "2020-08-06"
+++
Save and restore folds automatically:

```
augroup AutoSaveFolds
  autocmd!
  autocmd BufWinLeave * mkview
  autocmd BufWinEnter * silent loadview
augroup END
```

Defeult value for  `viewdir` is `~/.vim/views` on Unix
