# Managing Projects

Since I am mainly programming in Rust, I use the tmux-sessionizer, which is fully written in Rust.
The tool fits perfectly with my workflow.

# How to start?

I usually start my programming day with `tms switch`, which shows me the sessions in tmux.

If I want to see all current projects I am working on, even those without an active tmux
session, I just run `tms`.

## How to add directories to search for projects to add to the tms list

You can use the `tms config -p <path>` to add them, or add them in the
config file `~/.config/tms/config.toml`

An example of a tms config file:

```bash
session_sort_order = "LastAttached"
[[search_dirs]]
path = "/home/alex/2025"
depth = 10

[[search_dirs]]
path = "/home/alex/book"
depth = 10
```

## Inside a session launch the tms session window

`<prefix> w`
`<prefix> s`

To select a session from the list you can use the up,down keys.
To leave escape.

## To rename a session

`<prefix> r`

It is short, but then again ... .

## How to kill a session?
