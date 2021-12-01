+++
title = "g command comments"
date = "2019-02-01"
+++
```vim
:g/_pattern_/s/^/#/g
```

will comment out lines containing `_pattern_` (if `#` is your comment character)

Another way of doing this is with normal commands instead of text substitution:

```vim
:%g/912150\|912147\|912145\|912157\|912155\|912151/norm I// 
```
<sub>_Note: there is a trailing space in this code block_</sub>

swap `g` with `v` at the beginning and it will comment out lines that _don't_ match the pattern.
