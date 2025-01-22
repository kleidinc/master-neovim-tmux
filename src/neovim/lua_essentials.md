# Lua Essentials

You don't need to be a master in lua to configure your Neovim. Just
some basics are enough.

### Pattern to add a Plugin to Neovim

1. Always read the documentation. You will find how to import and use the plugin.

2. Add key-maps via vim.keymap.set(--) for plugin-commands you intend to use

### An Example: Harpoon

```lua
return {
    "ThePrimeagen/harpoon"
    dependencies = { "nvim-lua/plenary.nvim" }
    config = function()
        local harpoon = require("harpoon")
        harpoon:setup()
        -- Add Telescope Support

        -- Add Keymappings
    end
}
```
