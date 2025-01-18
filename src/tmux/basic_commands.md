# Basic tmux commands

# Prefix

The standard prefix is `Control b`. I changed it to `Control space`. You can
set it to whatever you feel most comfortable with.

# How to get into the command line

`<prefix> :`

# Sessions

## How to open a new tmux session without a name

I rarely every use that ,because having a session without a name is unusable,
and you have to rename the session anyway afterwards. It's much better to
start a session with a name from the start.

`<prefix> c`

## How to start a new session with a name

`tmux new-session -s <name_of_session>`

<!-- TODO: fix -->

But you can't do that when you are already running a tmux-session.
You need to first detach from a session.

## How to detach from a session?

When you detach from a session you are not killing the session.
You can still re-attach to the session at any time.
`<prefix> d`

## How to attach to a session?

```bash
tmux attach -t <session_name>
```

## How to rename a session

## How to list all sessions

```bash
tmux list-sessions
tmux ls
```

## How to switch to a session

## How to kill a specific session?

```bash
tmux kill-session -t <session_name>
```

## How to kill all but the current session?

```bash
tmux kill-session -a
```

# Windows

# Panes

# Show the current time

`<prefix> t`
