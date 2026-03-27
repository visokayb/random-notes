# Tmux Commands

The general idea: tmux server -> session -> window -> pane

## Session Management

Create a new session:
```bash
tmux new-session -s session-name
``` 

Attach to a session:
```bash
tmux attach -t session-name
```

Kill a session:
```bash
tmux kill -t session-name
```

List sessions:
```bash
tmux ls
```

Attach by session number:
```bash
tmux attach <session number>
```

---

## Keyboard Shortcuts

**Default Prefix:** `Ctrl + b`

| Action | Shortcut |
|--------|----------|
| Enter copy mode (press `q` to exit) | `Ctrl + b, [` |
| Detach from session (without stopping it) | `Ctrl + b, d` |
| Split window horizontally | `Ctrl + b, %` |
| Split window vertically | `Ctrl + b, "` |
| Switch to pane in direction | `Ctrl + b, ↑ ↓ ← →` |
| Move current pane left | `Ctrl + b, {` |
| Move current pane right | `Ctrl + b, }` |
| Show pane numbers | `Ctrl + b, q` |
| Switch/select pane by number | `Ctrl + b, 0–9` |
| Toggle pane zoom | `Ctrl + b, z` |
| Convert pane into a window | `Ctrl + b, !` |
| Resize pane height | `Prefix, Ctrl + ↑ ↓` |
| Resize pane width | `Prefix, Ctrl + ← →` |
| Close current pane | `Ctrl + b, x` |
| Toggle between pane layouts | `Ctrl + b, Spacebar` |
| Switch to next pane | `Ctrl + b, o` |

---

## Splitting Panes

Split horizontally:
```bash
split-window -h
```

Split vertically:
```bash
split-window -v
````

Split vertically with 95% height:
```bash
tmux split-window -p 95
```

> You can use `-v` and `-h` switches for vertical and horizontal splits respectively. The `-p` switch specifies the percentage.

---

## Sources
- https://arcolinux.com/everthing-you-need-to-know-about-tmux-panes/
