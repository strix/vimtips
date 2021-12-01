+++
title = "hacker news links"
date = "2019-02-01"
+++
Get all the links from hacker news in vim:
```vim
:read !curl https://news.ycombinator.com
:v/https/d
:%s/^.*href="\(https.\{-}\)".*/\1/g
```
