# How to use Macrow

### What is a Macro?

A macro stores and replays the actions you take in nvim.
You can record a macro manually.

### Pattern to record and play a macro

1. `q<register>`
   The `register` is usually a letter or number, which represents the letter or number of the register you want
   the macro to be recorded at.

2. Then you perform the action once.

3. `q` to save the macro.

4. `@<register>`

Let's say we choose the register `a` then the command to start recording would be `qa` and to replay `@a`.

### Pattern to apply a macro on multiple lines?

Just prepend it with the <lines_amount>. For example if you want to apply the macro a to 4 lines, just
type `4@a`.
