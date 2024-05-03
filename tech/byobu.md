This cheat sheet delivers a detailed guide on **Byobu keybindings**, essential for efficient terminal multiplexing. It covers an extensive range of commands for creating and managing windows, splits, and sessions, from basic navigation to advanced configuration options. Additionally, **it includes tailored keybindings for Byobu over SSH, specifically for users on Windows using Putty and macOS using Terminal, to Ubuntu**, ensuring accessibility and ease of use across different platforms.

## Byobu Keybindings

### F1

- **Shift-F1**: Display this help.

### F2

- **Shift-F2**: Create a horizontal split.
- **Ctrl-F2**: Create a vertical split.
- **Ctrl-Shift-F2**: Create new session.

### F3/F4

- **Alt-Left/Right**: Move focus among windows.
- **Alt-Up/Down**: Move focus among sessions.
- **Shift-Left/Right/Up/Down**: Move focus among splits.
- **Shift-F3/F4**: Move focus among splits.
- **Ctrl-F3/F4**: Move a split.
- **Ctrl-Shift-F3/F4**: Move a window.
- **Shift-Alt-Left/Right/Up/Down**: Resize a split.

### F5

- **Alt-F5**: Toggle UTF-8 support, refresh status.
- **Shift-F5**: Toggle status lines.
- **Ctrl-F5**: Reconnect ssh/gpg/dbus sockets.
- **Ctrl-Shift-F5**: Change status bar's color randomly.

### F6

- **Shift-F6**: Detach session and do not logout.
- **Alt-F6**: Detach all clients but yourself.
- **Ctrl-F6**: Kill split in focus.

### F7

- **Alt-PageUp/PageDown**: Enter and move through scrollback.
- **Shift-F7**: Save history to $BYOBU_RUN_DIR/printscreen.

### F8

- **Ctrl-F8**: Rename the current session.
- **Shift-F8**: Toggle through split arrangements.
- **Alt-Shift-F8**: Restore a split-pane layout.
- **Ctrl-Shift-F8**: Save the current split-pane layout.

### F9

- **Ctrl-F9**: Enter command and run in all windows.
- **Shift-F9**: Enter command and run in all splits.
- **Alt-F9**: Toggle sending keyboard input to all splits.

### F10

_No commands specified._

### F11

- **Alt-F11**: Expand split to a full window.
- **Shift-F11**: Zoom into a split, zoom out of a split.
- **Ctrl-F11**: Join window into a vertical split.

### F12

- **Shift-F12**: Toggle on/off keybindings.
- **Alt-F12**: Toggle on/off mouse support.
- **Ctrl-Shift-F12**: Mondrian squares.

##Byobu (over SSH
### Windows + Putty to Ubuntu

| Action                              | Windows + Putty to Ubuntu | 
| ----------------------------------- | ------------------------- | 
| Help menu                           | BASH: byobu-config        | 
| Create new window                   | CTRL-a c                  | 
| Previous window                     | CTRL-a p                  | 
| Next window                         | CTRL-a n                  | 
| Detach                              | CTRL-a d                  | 
| **Window**                                    |                           | 
| Retitle window                      | CTRL-a A                  | 
| Move to window                      | CTRL-a \<N>               | 
| Kill windows/close                  | CTRL-a \                  | 
| Switch between 2 windows            | CTRL-a CTRL-a             | 
| **Pane**                                    |                           | 
| Add pane horizontal                 | CTRL-a %                  | 
| Add pane vertical                   | CTRL-a \|                 | 
| Add pane menu                       | CTRL-a >                  | 
| Switch panes                        | CTRL-a TAB                | 
| Menu to select window               | CTRL-a "                  | 
| **Scrollback**                                    |                           | 
| Scrollback mode                     | CTRL-a \[                  | 
| Buffer up/down (in scrollback mode) | PAGEUP / PAGEDOWN         | 
| Scrollback select                   | SPACE-ARROWS              | 
| Scrollback copy selected            | ENTER / RETURN            | 
| Paste copied text                   | CTRL-a ]                  | 
| **Close**                                    |                           | 
| Close window w/confirm              | CTRL-a k                  | 
| Close window/pane                   | CTRL-d or exit            | 

### MacOS + Terminal to Ubuntu

| Action                              | MacOS + Terminal to Ubuntu |
| ----------------------------------- | -------------------------- |
| Help menu                           | FN-F1                      |
| Create new window                   | CTRL-a c  or  FN-F2        |
| Previous window                     | CTRL-a p  or  FN-F3        |
| Next window                         | CTRL-a n  or  FN-F4        |
| Detach                              | CTRL-a d                   |
| **Window**                                    |                            |
| Retitle window                      | CTRL-a A                   |
| Move to window                      | CTRL-a \<N>                |
| Kill windows/close                  | CTRL-a \                   |
| Switch between 2 windows            | CTRL-a CTRL-a              |
| **Pane**                                    |                            |
| Add pane horizontal                 | CTRL-a %                   |
| Add pane vertical                   | CTRL-a \|                  |
| Add pane menu                       | CTRL-a >                   |
| Switch panes                        | CTRL-a TAB                 |
| Menu to select window               | CTRL-a "                   |
| **Scrollback**                                    |                            |
| Scrollback mode                     | CTRL-a \[                   |
| Buffer up/down (in scrollback mode) | FN-SHIFT-ARROWS            |
| Scrollback select                   | SPACE-ARROWS               |
| Scrollback copy selected            | ENTER / RETURN             |
| Paste copied text                   | CTRL-a ]                   |
| **Close**                                    |                           | 
| Close window w/confirm              | CTRL-a-k                   |
| Close window/pane                   | CTRL-d or exit             |

Source: [PackeTsar](https://gist.github.com/PackeTsar/e4adf2a2056710a0b65c537fd2990188)
