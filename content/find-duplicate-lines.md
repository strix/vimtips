+++
title = "find duplicate lines"
date = "2019-01-19"
+++
simple way to find duplicate lines in vim:

1. Sort the file using `:sort`
2. Execute command `:g/^\(.*\)$\n\1$/p`
