+++
title = "working with delimiters"
date = "2020-11-12"
+++
Use `c%` to change text within delimiters. Example:

```
link_to("text", my_path(singularize("one"), pluralize(double("two"))))
                ^      A                                            B
```

"It also handles `[]` square brackets, `{}` curly braces and some other things. It can be used as a standalone motion or with other operators than `c`.

For example, you could use `%d%` to change `remove_my_argument(BigDecimal(123))` into `remove_my_argument`."

[source](https://thepugautomatic.com/2014/03/vims-life-changing-c-percent/)
