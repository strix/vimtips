+++
title = "fix issues with delays"
date = "2020-05-27"
+++
In case there is any issue with delays when pressing escape or just keypresses in general. I remember experiencing this in the past and would be good to have it documented:

[vi escape delays](https://www.johnhawthorn.com/2012/09/vi-escape-delays/)

tl;dr:

vim: `set timeoutlen=1000 ttimeoutlen=0`

zsh: `KEYTIMEOUT=1`

tmux: `set -s escape-time 0`
