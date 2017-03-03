---
layout: page
title: Tmux
permalink: /resources/tmux/
---

# Installation

- To install tmux, use the provided package manager. Ubuntu is shown below:

```
$ sudo apt-get install tmux
```

# Commands

- Shortcut (Used to invoke all commands for tmux)

```
ctrl-b command
```

- Show Sessions `ctrl-b S` or `$ tmux ls`

- Create a New Session

```
$ tmux new -s session_name
```

- Attach to an Existing Session

```
$ tmux a -t session
```

- Kill a Session

```
$ tmux kill-session -t session-name
```

## Commands

| Command Code        | Description           |
| ------------- |:-------------:| 
|? |	help |
|s |	list sessions|
|$ |	rename current session|
|d |	detach current session|
|c |	create new window|
|, |	rename window|
|[ |	scroll through history|
|w |	list windows|
|% |	split vertically|
|" |	split horizontally|
|n |	change to next window|
|p |	change to previous window|
|o |	toggle between panes|
|0-9 |	select window 0 - 9|
|h |	move left|
|j |	move below|
|l |	move right|
|k |	move above|
|q |	show pane #'s|
|} |	swap with next pane|
|{ |	swap with prev pane|
|! |	break pane out of window|
|q # |	switch to pane number|
|x |	kill pane|
|t |	show time in pane|
|z |	min/max pane|


## Customizing tmux

You can customize tmux by modifying the `~/.tmux.conf` file.

For example if you wish to keybind the sync command, then you would place the following line in your tmux file:
```
bind e setw synchronize-panes
```
This keybinds Ctl-b e to toggle syncing panes on and off
