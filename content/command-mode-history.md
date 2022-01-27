+++
title = "command mode history"
date = "2022-01-26"
+++
use `q:` to access previously ran commands in command mode (`:`)

if you're already in command mode then you can do the same with `<C-f>`. This one is especially handy if you already have part of the command written out since using `<C-f>` will allow you to edit the in-progress command further but in a separate buffer with all other modes at your disposal.

This allows you to search and edit previously ran (or even the current, in-progress command). Press `enter` to execute the command under the cursor.

You can exit this mode without any effect by hitting `enter` on an empty entry (`q:` will start on an empty entry).
