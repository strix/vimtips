+++
title = "paste with indent"
date = "2023-04-01"
+++
Even if you have an indent blankline plugin installed, sometimes pasting will go to the wrong indentation level. To help alleviate this, you can use `]p` (before the current line) and `[p` (after the current line) to paste at the same level as the currently selected line.

So a normal paste behaves like this (even with a blankline plugin):
```
text text <-- yy
  indented text <-- on this line p
text text <-- result
```

But using `[p` and `]p`, the indentation is kept at the same level of the currently selected line when the command was issued:
```
text text <-- yy
  text text <-- result using [p
  indented text <-- on this line [p or ]p
  text text <-- result using ]p
```

Before discovering this, I would use a custom `gp` keybind to [reselect last pasted text](@/reselecting-text.md) and then hit `=` once the text was selected to reindent the incorrectly indented text. By using `[p` and `]p`, I can skip those extra keystrokes.
