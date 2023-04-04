+++
title = "search delimiter"
date = "2023-04-01"
+++
You can use any regex delimiter in your pattern substitution. No need to use `/` at all, try `#` instead. The following are equivalent:

```vim
:%s/find/replace/gc
:%s#find#replace#gc
```

Super useful for when you want to include `/` characters in your search and can avoid escaping them:

```vim
:%s/\/route\/path/\/new_route\/new_path/gc
:%s#/route/path#/new_route/new_path#gc
```
