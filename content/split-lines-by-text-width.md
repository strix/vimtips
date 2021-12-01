+++
title = "split lines by text width"
date = "2021-07-06"
+++
Split lines with `gq`
- In visual mode, it will split whatever is selected.
- In normal mode, you follow `gq` with a motion.

For example, `gql` will split one line to the currently set width. To set the width of the split lines to be different from your current setting, you can use

`:set textwidth=<n>`

Where n=number of characters you want in a line, e.g., 10, and change back to your normal width when you're done.
