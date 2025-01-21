# How to Efficiently Navigate Large Files

When you build serious things, files often become very large
and difficult to navigate. Here are some tips on how to stay
productive.

## Marks

The most efficient way when you are working with large files, is
to set marks, at functions, structs, enums, ... you are working
on. Then you can easily move back and forth. This will speed up
coding, and is a real productivity boast.

### How to Set a Mark

`m + <lowercase_letter>` -> this will set a marker / m a

- Lowercase letters are used for marks if you only want to set a mark,
  accessible when you are inside the document.
- Capital letters are used, when you want the mark to be accessible
  from outside the file.

### How to Jump to a Mark

If you remember the mark, you can just perform:

`' + <letter_of_the_mark>` (quote + name of the mark) / 'a

If you don't remember, `Telescope marks`, which lists all current marks
in your project.

### How to Delete a Mark from Telescope?

## Navigate by Line Numbers

Often the compiler will compain, and list a line number and a column.
You can easily jump to any needed location in a file with the following
short-cuts.

## How to jump to a specific line

<line_number> Capital G

Is faster then :<line_number> carriage return

## How to collate two lines together

### with a space between them

Capital J - which joins two lines with a space between them

### without a space between them

g Capital J
