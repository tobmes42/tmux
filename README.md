# tmux

Copy the tmux.conf to your homefolder and make it hidden.

```bash
cp tmux.conf ~/.tmux.conf
```

start new:

    tmux

start new with session name:

    tmux new -s myname

attach:

    tmux a  #  (or at, or attach)

attach to named:

    tmux a -t myname

list sessions:

    tmux ls

kill session:

    tmux kill-session -t myname

In tmux, hit the prefix `ctrl+b` and then:

## Sessions

    :new<CR>  new session
    s  list sessions
    $  name session

## Windows (tabs)

    c           new window
    ,           name window
    w           list windows
    f           find window
    &           kill window
    .           move window - prompted for a new number
    :movew<CR>  move window to the next unused number

## Panes (splits)

    |  horizontal split
    -  vertical split
    
    o  swap panes
    q  show pane numbers
    x  kill pane
    ⍽  space - toggle between layouts

## Window/pane surgery

    :joinp -s :2<CR>  move window 2 into a new pane in the current window
    :joinp -t :1<CR>  move the current pane into a new pane in window 1

* [Move window to pane](http://unix.stackexchange.com/questions/14300/tmux-move-window-to-pane)
* [How to reorder windows](http://superuser.com/questions/343572/tmux-how-do-i-reorder-my-windows)

## Misc

    d  detach
    t  big clock
    ?  list shortcuts
    :  prompt
    
    
## Copy mode (vi mode)

    Prefix [ - start copy mode
    Prefix ] - past from copy mode
    ^ - back to indentation
    esc - clear selection
    enter - copy selection
    j - cursor down
    h - cursor left
    l - cursor right
    k - cursor down
    L - cursor to bottom line
    M - cursor to middle line
    H - cursor to top line
    d - delete entire line
    D - delete to end of line
    $ - end of line
    : - goto line
    ⌃-d - half page down
    ⌃-u - half page up
    ⌃-f - next page
    w - next word
    p - paste buffer
    ⌃-b - previous page
    b - previous word
    q - quit mode
    ⌃-down, ⌃-j - scroll down
    ⌃-up, ⌃-k - scroll up
    n - next search match
    ? - search backward
    / - search forward
    0 - start of line
    space - start selection
