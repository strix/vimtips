+++
title = "quickfix list commands"
date = "2020-01-20"
+++
Run the command to each line of the quickfix list:

```vim
:Ack pattern
:cdo s/pattern/newpattern/g
```

Note: `cdo` is for executing a command on each entry in the quickfix list, `cfdo` is for executing a command for each file in the quickfix list.
