# Jupyter on Rust

to check later [another mirror impl](https://neovimcraft.com/plugin/SUSTech-data/neopyter/)

### Installing EvCxR

```bash
# Install the classic Jupyter notebook
pip install notebook
#
cargo install --locked evcxr_jupyter
evcxr_jupyter --install
cargo install --locked evcxr_repl
# By default will install in $HOME/.local/share/jupyter/kernels/
rustup component add rust-src
# To run jupyter in the classic way in the browser `jupyter notebook`
```

### Install Rust Crates for ML/AI

```bash
cargo install ndarray
cargo install plotly
```

#### How to list which Jupyter kernels you have installed?

`jupyter kernelspec list`

### Install Neovim plugins for Jupyter

#### [molten.nvim](https://github.com/benlubas/molten-nvim/blob/main/docs/Not-So-Quick-Start-Guide.md)

The installation and user guide of Molten is to good to repeat here.

#### `jupytext.nvim`

#### [image.nvim](https://github.com/3rd/image.nvim)

```lua
return {
    "3rd/image.nvim",
    build = false,
    opts = {

    }
}
```

### Polars still to be installed

### Workflow of using Jupyter inside Neovim

1. start the jupyter server
2. start a notebook
3. connect automatically to the jupyter server
