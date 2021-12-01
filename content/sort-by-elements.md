+++
title = "sort by elements in a list"
date = "2021-03-22"
+++
If you want to sort lines based on the second element on the list:

```
pancake, donut, waffle
sushi, pasta, taco
apple, banana, carrot
water, apple juice, milk
```
Run:
`:sort /,/`

Vim will use the characters after the match to sort.

```
water, apple juice, milk
apple, banana, carrot
pancake, donut, waffle
sushi, pasta, taco
```
