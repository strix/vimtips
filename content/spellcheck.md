+++
title = "spellcheck"
date = "2023-04-01"
+++
Enable spellcheck by running:
```vim
:set spell
```

Turn if off with:
```vim
:set nospell
```

Or toggle it with:
```vim
:set spell!
```

Use `[s` and `]s` to navigate to the previous and next misspelled word. While the cursor is on the misspelled word, use `z=` to get a list of correction suggestions.

Use `zg` to add a word to the dictionary and use `zw` to remove a word from the dictionary.
