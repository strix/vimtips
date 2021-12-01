+++
title = "show whitespace characters"
date = "2021-07-01"
+++
To show whitespace characters use:

```vim
set list (set nolist to hide it)
```

To determine which characters show up as whitespace (since the defaults suck) you can set them with this:

```vim
set showbreak=↪
set listchars=eol:¬,tab:>·,trail:~,extends:>,precedes:<,space:␣
```
