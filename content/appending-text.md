+++
title = "appending text"
date = "2020-12-21"
+++
`A` to append to end of line.

Use `$A` in visual block mode to append to the end of each line regardless of different line lengths.

This can also be done by pressing `:` while in visual block mode with the resulting command like the following:

```vim
:'<,'>s/$/[appended-text-here]/
```
