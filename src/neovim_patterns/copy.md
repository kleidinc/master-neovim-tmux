# How to copy something

### Pattern to copy a word

`viw`
`V`isually Highlight `i`n `W`ord

`y`ank to put that word to a register

Go to the place where you want to copy that word and
press `p`aste, to paste it.

### Pattern to copy data from previously yanked data

All data you yank, copy or delete, goes to a register.

`:reg` this will show all the yanked, copied, deleted data in a
numbered way.

You can still paste any of the data still in the register.
`"<number_of_the_register>p`

So if you want to paste the 5th register, you would type
`"5p`

### Pattern to yank text to a specific register location

`"<number>y`

# Pattern to use the \+Register, the system clipboard

This allows you copy something from nvim, into other programs.

`"+y` places text into the clipboard.
