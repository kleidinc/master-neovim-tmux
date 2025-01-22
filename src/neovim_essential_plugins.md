# Essential Plugins For Distraction Free Coding

### [Context]()

to find and install

### [Harpoon]()

Easier way to just between files in a project. You can add files and then with a
shortcut jump from one file to another. That way you can bypass NvimTree and even
Telescope when you are working on a limited amount of files.

<!-- TODO: Install -->

### [Focus](https://github.com/cdmill/focus.nvim?tab=readme-ov-file)

You can remove everything except the line numbers. This will help you get into
a state of total focus and stay in it for hours on end, without even noticing.

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

### [Marks](https://github.com/chentoast/marks.nvim)

Marks are very important when navigating through large files, and projects. This plugin
improves the standard experience.
