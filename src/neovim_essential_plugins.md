# Essential Plugins

### [Focus](https://github.com/cdmill/focus.nvim?tab=readme-ov-file)

This is my plugin of choice to code distraction free. You can remove everything except the
line numbers. This will help you get into a state of total focus and stay in it for hours
on end, without even noticing.

I have the `:Focus` command mapped to to `<leader>fo` fo for focus. It removes the status-bar
for both neovim, tmux and the diagnostics.

It is very annoying to see diagnostic errors as you are typing. My workflow is mostly
firt coding and only after I finished the structure, I deactivate focus mode, and go
through the diagnostics.

### [Twilight](https://github.com/folke/twilight.nvim)

This plug works alongside the Focus plugin to even further focus on the the block
you are programming, and dimming everything else.

You can enable twilight in the opts of the Focus plugin by uncommenting the
line:

```bash
plugins = {
    -- twilight = { enabled = true }, -- enable to start Twilight when zen mode opens
  },
```
