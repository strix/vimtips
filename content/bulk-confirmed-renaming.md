+++
title = "bulk, confirmed text replacement"
date = "2021-11-09"
+++
This was handy for bulk, confirmed renaming, I used telescope's live_grep feature to put the results in a quickfix list (although any other method for populating a quickfix list would work) and then ran:

```vim
:cfdo %s/find/replace/gce | %s/findanother/replaceanother/gce | %s/findyetanother/replaceyetanother/gce | update
```

to do multiple replacements on the files in the quickfix list and then saved them all with `update`. I could've saved them all with `:cfdo w` as well.
