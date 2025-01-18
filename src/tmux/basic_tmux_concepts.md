# tmux

# Manual help

```bash
man 1 tmux
```

# Basic Concepts

tmux keeps all its state in a single main process. This runs in the background and
manages all the programs running inside tmux and keeps track of their output.

The tmux server is started automatically when the user runs a tmux command and by
default exits when there are no running programs.

Users attach to the tmux server by starting a client. This takes over the terminal
where it is run and talks to the server using a socket file in /tmp.

Each client runs in one terminal, which may be an X terminal such as xterm, the
system console, or a terminal inside another program (such as tmux itself).

Each client is identified by the name of the outside terminal where it is started,
for example /dev/ttypf.

# Sessions, windows and panes

Every terminal inside tmux belongs to one pane, this is a rectangular area which shows
the content of the terminal inside tmux. Because each terminal inside tmux is shown in
only one pane, the term pane can be used to mean all of the pane, ther terminal and the
program running inside it.

Each pane appears in one window. A window is make up of one or more panes.

Every window has a name - by default tmux will choose one but it can be changed
later by the user. Window names do not have to be unique, windows are usually identified
by the session and the window index rather than their name.

Each pane is separated from the panes around it by a line, this is called the pane
border. There is one pane in each window called the active pane, this is where any
text types is sent and is the default pane used for commands that target the window.

The pane border of the active pane is marked in green, or if there are only two
panes then the top, bottom, left or righ thalf of the border is green.

Multiple windows are grouped together into sessions. If a window is part of a session,
it is said to be linked to that session.
Windows may be linked to multiple sessions at the same time, alhtough mostly they are
only in one. Each window in a session has a number, called the window index - the same
window may be linked at different indexes in different sessions.

A session's window list is all the windos linked to that session in order of their
indexes.

Each session has one current window, this is the window displayed when the session is
attached and is the default window for any commands that target the session. If the
current window is changed, the previous current window becomes known as the last
window.

A session may be attached to one or more clients, which means it is shown on the outside
terminal where that client is running. Any text typed into that outside terminal is sent
to the active pane in the current windown of the attached session.

## In Summary

- Programs un in terminals in panes, which each belong to one window.
- Each window has a name and one active pane.
- Windows are linked to one or more sessions.
- Each session has a list of windows, each with an index.
- One of the windows in a session is the current window.
- Sessions are attached to one or more clients, or are detached (attached to other clients).
- Each client is attached to one sesssion.
