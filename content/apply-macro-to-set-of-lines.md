+++
title = "apply a macro only to a set of lines"
date = "2021-12-01"
+++
Use the normal command in Ex mode to execute the macro on multiple/all lines:

Execute the macro stored in register a on lines 5 through 10.

```
:5,10norm! @a
```

Execute the macro stored in register a on lines 5 through the end of the file.

```
:5,$norm! @a
```

Execute the macro stored in register a on all lines.

```
:%norm! @a
```

Execute the macro store in register a on all lines matching pattern.

```
:g/pattern/norm! @a
```

To execute the macro on visually selected lines, press `V` and the `j` or `k` until the desired region is selected. Then type `:norm! @a` and observe that the following input line is shown.

```
:'<,'>norm! @a
```

Enter `:help normal` in vim to read more.

[source](https://stackoverflow.com/a/390194/4263710)
