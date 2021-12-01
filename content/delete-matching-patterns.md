+++
title = "delete matching patterns"
date = "2019-11-06"
+++
Delete all lines not matching a pattern:

```vim
:%g!/912150\|912147\|912145\|912157\|912155\|912151/d
````

In this example, all lines not containing these numbers will be deleted.
