+++
title = "duplicating files"
date = "2020-11-23"
+++
This is something I would always leverage a file tree plugin for. I can't find a good way to accomplish this with my current file tree plugin (NvimTree) so finding a native, effective way without plugins was needed.

Method 1: You can open the new file first and then copy the original file into the buffer

``` vim
:e another-file
:r original-file
```

Method 2 (my personal favorite): use `:sav duplicated-file` while in the file you want to duplicate.

```vim
:sav[eas][!] [++opt] {file}
            Save the current buffer under the name {file} and set
            the filename of the current buffer to {file}.  The
            previous name is used for the alternate file name.
```
