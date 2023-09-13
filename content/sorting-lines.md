+++
title = "sorting lines"
date = "2020-11-08"
+++
There are multiple ways to sort lines in Vim. Here is a short and useful list:

```vim
# to sort all the lines in the file, alphabetically
:sort
# to sort all the lines but in reverse
:sort!
# removes duplicate lines while sorting
:sort u
# ignores the case when sorting
:sort i
# sorts numerically to prevent 100 from coming before 20
:sort n
```

To sort starting from line 6 to the end of the file, run: `:6,$sort`

You can also sort just the lines that are visually selected.
