# Essential Commands

## how to save and quit

ZZ

## How to quit without saving

ZQ

## How to select the content between {} or ()

vib
viB

## How to change everything between the "" or {}

ciB

## How to put something in front of many lines at the same time

1. Go into Visual Block Mode : Ctrl+v
2. Navigate to the end of the block
3. Go into Insert Mode : Capital I
4. Type what you want to add on the first entry
5. Copy it in front of all the lines : Esc

## How to put something on the back of many lines with different length

1. gv - this will select the last highlighted text
2. $ - to select until the end of all the lines
3. Capital A - to append to the end
4. type what you want to type at the end of the first line
5. Escape - and this will append it on all the lines

## How to turn a word in to CAPITALS

1. g` (tilde) to turn a letter into Capital
2. w to apply the tilde highercase action to the whole word
   or
3. it for putting everything inside the inner tag into highercase

## How to navigate to the end of a {} or a []

1. type %

## How to save the current nvim session so the next time you can load it again

1. :mksession somefile.vim

Next time you can

2. :source somefile.vim and the session will be loaded again

## How to indent a file

1. gg to go to the top of the file
2. =
3. Capital J to select and indent the whole file

## How to open an existing file under a cursor in neovim

gf

## How to open a URL under the cursor in a browser window

gx
