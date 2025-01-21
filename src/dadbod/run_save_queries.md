# Queries inside Neovim

### How to save a query (from the buffer)?

When you create a new query, it remains temporary in the buffer. After restarting neovim, the buffer is
cleared and so your query will be gone.

If you run this query regularly you can name, and save your query by pressing
`<leader> W`.

Or you can remap `DBUI_SaveQuery` to another keymap.

### How can you execute a query?

`<leader>S`

Or remap `:DBUI_ExecuteQuery` to another keymap.

### How to re-execute all queries?
