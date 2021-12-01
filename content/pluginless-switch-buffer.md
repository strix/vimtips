+++
title = "switch buffers without a plugin"
date = "2021-08-30"
+++
One way to switch buffers without using any plugin is to use:

`:buffer BUFFERNAME`

One keymap that you can use:

```vim
nnoremap <Leader>b :buffer<Space>
```

Then you can press TAB and select the buffer you want to go into

[source](https://twitter.com/learnvim/status/1432379361622102016?s=19)
