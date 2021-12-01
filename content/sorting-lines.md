+++
title = "sorting lines"
date = "2020-11-08"
+++
You can sort lines with Vim's `sort()` command. To sort the entire buffer, simply run:

```vim
:sort
```

To sort starting from line 6 to the end of the file, run: `:6,$sort`

You can also sort just the lines that are visually selected.
