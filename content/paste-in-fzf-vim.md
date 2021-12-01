+++
title = "paste in fzf.vim prompt"
date = "2021-06-07"
+++
Figured out a solution to that paste in fzf thing btw. So it turns out that fzf just runs in a terminal popup so it's the same keybindings for the :term mode. So you can paste the current clipboard the manual way with `<C-w>"+` or map that to a keybind using `tnoremap <custom-binding-here> <C-w>"+`.
