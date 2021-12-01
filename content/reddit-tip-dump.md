+++
title = "reddit tip dump"
date = "2021-07-27"
+++
**NOTE A lot of these are duplicates of tips already discovered/shared but figured I'd dump them all here anyway.**

**All of the following come from [this reddit thread](https://www.reddit.com/r/vim/comments/osednx/lesser_known_vim_functionality/). It might be worth checking out again as there might be more that trickle in there.**

---
The `.` key actually has a special behavior with the number registers `”0` To `”9`. Specifically, if the change that the `.` command is repeating references a number register, the `.` command will actually increment the referenced register after running. This is a little hard to explain, but try doing this:
1. `”1p`
2. `u.`

Repeat `u.` as many times as you’d like.

This will cycle through the number registers, starting with register 1, putting it, then undoing it, then putting register 2, undoing it, etc.

Why is this useful? The number registers contain your last deletes! If you want to recover some accidentally deleted text, you can repeat the steps above until you get the text you want.

---

`g<C-a>` - in visual mode invokes `<C-a>` command for every line n times, where n is number of line in visual selection.
Very useful for creating numbered lists:
Create 10 lines with 0. at the beginning `10o0.<esc>`
Select paragraph `vip`
Use `g<C-a>`.
You get list from 1 to 10.

---

Vim has many marks & lists that it stores positions automatically.

Marks:
`'<` & `'>` start/end of visual selection

`'[` & `']` - start/end of last change or yank

`'.` - position of where last change was made

`'^` - position of cursor when last Vim last left insert mode - This is how gi command works

`''` - position before last jump (Super useful!). See :h ''

Use `g;`/`g,` to move through the changelist positions (I use this all the time)

`<c-o>`/`<c-i>` to move through the jumplist

`:visual o/O` … flip selection “caret”

`gv` … reselect previous visual selection

`/foo/e` … end of search rather than beginning. Also see :help search-offset

`//` … “search for the last search” (eg: `:%s//XXX/g` … replace last search with XXX)

`g/foo/norm A,<esc>0fxietc`…etc…like a macro`<cr>`

…basically there are a few ways to invoke :norm … which lets you kind of “just do what you want” on matching lines. With the search-offset functionality mentioned above, you can do some wizardly efficient editing.

`<C-w><C-r>` = rotate splits

The `&` command in normal mode repeats the last "`:s/`" command (without flags) on the current line. There's also g& which does the substitute (using the most recent search) on every line with the same flags. They seemed like dumb niche things, but I found myself using them remarkably regularly.

`:help &`
`:help g&`

A "range" (:help :range) for an Ex command can accept all sorts of modifying ranges like /pattern/- to refer to the line before the next "pattern" or ?pattern?+3 to refer to 3 lines after the previous "pattern". And they can chain such as `?pattern1?/pattern2/-2` to search backwards for "pattern1" and then search forward for "pattern1" and then move back two lines. These can also include marks (e.g. "<+2 refers to two lines after the beginning of the most recent selection)

The {cmd} that follows a `:g` command can take a range relative to the match:

`:{range1}g/{regex}/{relative_range}{cmd}`
Want to delete every paragraph containing the word "carrot"?

`:g/carrot/'{+,'}d`
Want to indent 3 lines after each "carrot" to one line before the following "pepper"?

`:g/carrot/+3;/pepper/- >`
I use this one all the time and love it :-)

Related to the `:g` command, here’s another one that people often miss — you can chain `:g` and `:v` commands.

For example, `:g/foo/g/bar/d` deletes every line matching both foo and bar. `:g/foo/v/bar` deletes every line that matches foo but not bar. The great thing is, you can chain this as many times as you want!

I have used this in the past to delete all functions that don’t contain the word foo, for instance. Something like `:g/^func/v/foo/norm!V$%d`.

---

`ciw + ctl-r 0` - This makes the paste repeatable by not yanking the pasted over text.
