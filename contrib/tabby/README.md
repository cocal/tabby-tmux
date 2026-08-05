# Tabby clipboard helper

This directory contains a small tmux setup for Tabby on macOS.

It keeps `mouse on` so pane scrolling behaves normally, and copies selected
text to the local clipboard with OSC 52.

Install the helper script somewhere in your `PATH`:

```sh
mkdir -p ~/.local/bin
install -m 755 tmux-tabby-osc52-copy ~/.local/bin/
```

Then either run tmux with `-f contrib/tabby/tmux-tabby.conf`, or source the
fragment from your own config and keep the helper script in `PATH`.

If you use `~/.local/bin`, make sure it is on your `PATH`.

Example:

```sh
tmux -L tabbycopy -f /path/to/tabby-tmux/contrib/tabby/tmux-tabby.conf new -s work
```
