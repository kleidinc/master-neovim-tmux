# tmux

If you really want to take your coding toolkit to the next level you should add tmux to the mix.
tmux is an efficient way to manage terminal sessions and projects.

Practically this means that you always can return to the last state of your development environment
and continue coding without distractions.

## Benefits of combining tmux with neovim

- You can efficiently switch back and forth between projects by keyboard shortcuts you can customize.
- You can connect to your development environment from anywhere and continue working as if you were working on your computer.
- You can split your terminal into many windows, pane's and navigate efficiently between them using shortcuts you can define yourself.
- Both tmux, neovim, and all the plugins are open source, and if needed you can even customize and extend them.

## Installing tmux

Just like with neovim, you shouldn't just copy someone else's tmux config. Go through
the process. Just like with neovim you can install plugins, add key-maps, change the theme,
to fully customize your tmux experience.

You can even combine your tmux shortcuts and some plugins together.

## Kickstart your tmux fast(er)

If you want to start using tmux immediately, you can just study my base `.tmux.conf` config, and
copy it to your home directory `~/.tmux.conf`.

```bash
# Change from what directory tmux splits
bind '"' split-window -v -c "#{pane_current_path}"
bind % split-window -h -c "#{pane_current_path}"

# Change the way you can select and yank (copy) text, similar to nvim
set-window-option -g mode-keys vi
# Keybindings
bind-key -T copy-mode-vi v send-keys -X begin-selection
bind-key -T copy-mode-vi C-v send-keys -X rectangle-toggle
bind-key -T copy-move-vi y send-keys -X copy-selection-and-cancel

# Start the counting of windows at 1 instead of 0
set -g base-index 1
set -g pane-base-index 1
set-window-option -g pane-base-index 1
set-option -g renumber-windows on

# Enable mouse support
set -g mouse on

# Set a different prefix from Control + b
unbind C-b
set -g prefix C-Space
bind C-Space send-prefix

# Make sure the colors are good?
set-option -sa terminal-overrides ",xterm*:Tc"
# Custom key bindings
# Shift + Alt + h or l key
bind -n M-H previous-window
bind -n M-L next-window

# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'christoomey/vim-tmux-navigator'
set -g @plugin 'dreamsofcode-io/catppuccin-tmux'
set -g @plugin 'tmux-plugins/tmux-yank'
# enable ressurecting of tmux environments even after system reset
set -g @plugin 'tmux-plugins/tmux-resurrect'
set -g @plugin 'tmux-plugins/tmux-continuum'
# enable session manager
set -g @plugin 'omerxx/tmux-sessionx'

# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'github_username/plugin_name#branch'
# set -g @plugin 'git@github.com:user/plugin'
# set -g @plugin 'git@bitbucket.com:user/plugin'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
```
