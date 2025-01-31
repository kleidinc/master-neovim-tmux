# Inlay hints

As of neovim version 0.10 the inlay hints are built in. So you won't need to
add any plugins for that. By default they are turned off, as they clutter up
the screen.

Moreover for Rust, you will see that it doesn't operate perfectly (yet). You
can activate inlay-hints by adding 2 keymaps to your keymaps. But they will
appear only when you start editing the file.

### Why would you want inlay hints

For Rust it immediately gives the types of all variables. So if you are debugging
this is a great way to go through your code.

### How to activate?

Just add the following key-maps, with your custom shortcuts. I use *i*nsert *h*ints,
and *r*emove *h*ints.

```lua
--- To turn inlay hints on
keymap.set("n", "<leader>ih", function()
  vim.lsp.inlay_hint.enable(true, { 0 })
end, { desc = "lsp inlay hints on" })
--- To turn them off
keymap.set("n", "<leader>rh", function()
  vim.lsp.inlay_hint.enable(false, { 0 })
end, { desc = "lsp inlay hints off" })
```

Note: When learning, don't automatically use these hints, as you need to let your
brain work. I only use it occassionally. I prefer using 'K'.
