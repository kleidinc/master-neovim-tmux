# Jupyter on Rust

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

### Install Neovim plugins for Jupyter

#### `molten.nvim`

#### `jupytext.nvim`

#### `image.nvim`
