+++
title = "scrollbind"
date = "2019-10-22"
+++
When you are displaying more than one buffer in the same window, you can set the scrollbind option in each buffer so they scroll together.

In each buffer that should scroll simultaneously, enter the command:

`:set scrollbind`

You can enter `scb` as an abbreviation for `scrollbind`, and the `!` flag causes `:set` to toggle a boolean option. Therefore, it is convenient to enter the following to toggle `scrollbind` on or off:

`:set scb!`

use the `:diffthis` command to initiate a diff when Vim is already running.

e.g. file is open, open new file in split screen, invoke diff mode in both splits with `:diffthis` and turn it off with `:diffoff`.
