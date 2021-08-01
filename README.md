# Advanced Alt+Tab Window Switcher
Extension for Gnome Shell, a replacement of default Window Switcher Popup

*Advanced Alt+Tab Window Switcher* offers effective navigation between windows, including direct window activation, type to search mode, various filtering and sorting settings, workspace switching and hotkeys for window control.

## Features:

- **Type to Search mode** - you can activate it by a hotkey or you can set in preferences to start the switcher directly in this mode, so you can type immediately as the popup shows up and window list is filtered accordingly.
- Optional default filter settings : *All windows / Current workspace / Current monitor*, plus *Skip minimized* option.
- Optional default sorting settings: *Most Recently Used / Stable sequence / Stable sequence - current window first*.
- Optional default grouping settings: *None / Current workspace first / Applications / Workspaces*.
- Filter, sort and group modes can be switched on the fly by hotkeys when needed.
- Switching current workspace using a hotkey or a mouse scroll wheel outside the switcher popup.
- Sort and iterate through window list by applications instead of windows by hotkey
- Customizable window preview and app icon sizes. The larger one is used as the base and the smaller as the front icon.
- `Always on Top` property of selected window can be controled from the switcher and is indicated by the TOP position of the icon (or the preview if smaller) instead of default BOTTOM.
- The `view-pin` icon indicates whether the window is set as `Always on Visible Workspace` and you can control it from the switcher.
- Optional workspace index on each window item.
- Direct window activation via `F` keys with optional `F` key indicator on each window in the list.
- Optionaly windows can be brought to the front immediatey as they are selected, otherwise you can press dedicated hotkey to do it.
- Make live window previews as thumbnails that you can place anywhere on the screen and are always on top. This thumbnails can be controlled and can control the source window as described below.

## Installation:

Click on following badge to get it on extensions.gnome.org:

[<img alt="" height="100" src="https://raw.githubusercontent.com/andyholmes/gnome-shell-extensions-badge/master/get-it-on-ego.svg?sanitize=true">](https://extensions.gnome.org/extension/4412/advanced-alttab-window-switcher/)

### Hotkeys

    H/L, Left/Right         - window selection
    J/K, Up/Down, PgUp/Down - workspace selection
    Space, KP_0/KP_Ins      - Show selected window - switch to window workspace and bring it to the front
    Q                       - Switch window filter mode - ALL / WS / MONITOR
    ;/~/` (key above Tab)   - Sort windows by applications, each subsequent key press jumps to the first window of the next app
    G                       - Toggle sort by workspaces, when base filter is set to ALL
    1/+/!                   - Filter out all windows that don't belong to the application of selected window
    E/Insert                - Activate the Search mode, the `Insert` key can turn it off.
    W                       - Close selected window
    Shift+Del               - Force close - kill -9 to application of selected window
    C                       - Close all windows from window list that belong to the same application as selected window
    A                       - Toggle window 'Always on Top'. Also switch to window workspace and rise the window.
                               Indicated by the front icon on top instead of bottom.
                               When you press the 'A' key twice, it's actually equivalent to one press of hotkey for 'Show selected window'
    S                       - Toggle window 'Always on Visible Workspace', indicated by the 'pin' icon
    X/click outside switcher- Move selected window to the current workspace and to the monitor with mouse pointer
    N                       - Create New Window of selected application, if the app soupports it.
    V                       - Move window to selected workspace and maximize it.
    F                       - Move window to empty workspace next to its current workspace and switch it to fullscreen mode.
                               Next use of this action on the same window moves the window back to its original workspace and turn off the fullscreen mode.
    O                       - Show application grid, if you need to launch new application.
    T                       - Creates an thumbnail preview of selected window and place it to the bottom right of the current monitor.
                               You can move the thumbnail anywhere on the screen and you can make as many thumbnails you want
    P                       - Open preferences window for this extension

### Type to Search

When the `Search mode` is activated (by `E` or `Insert` keys or as default mode in preferences window), the keyboard keys `A-Z` and `0-9` can be used to type a pattern which will be searched for in the window title and application name, window list will be filtered accordingly. Characters with diacritics in the title and app name will be converted to the basic form and case doesn't matter. You can type in more patterns in arbitrary order separated by a space, so if you enter 'fox ext' window with 'Extensions - Firefox' in the title will be found too. If you type in a character that would filter out all windows, this character will be removed and the selection will stay unchanged waiting for another character.

**Even in the search mode you can use all hotkeys if you press and hold the Shift key**.

### DND Window Thumbnails

Window thumbnails are scaled-down window clones that can be used to monitor windows not currently visible on the screen. By pressing `T` hotkey you can create thumbnail of the selected window and place it at bottom right of the monitor with mouse pointer. You can create as many clones as you want and place them anywhere on the screen. Each thumbnail can be independently resized, you can adjust its opacity, even change its source window. When the thumbnail's source window close, thumbnail will be removed.

    Double click          - activate source window
    Primary cLick         - toggle scroll wheel function (resize / source)
    Scroll wheel          - resize or switch source window
    Ctrl + Scroll wheel   - switch source window or resize
    Secondary click       - remove thumbnail
    Middle click          - close source window
    Shift + Scroll wheel  - change thumbnail opacity
 
![Window Switcher Popup](screenshot.png)
![Extension configuration window](screenshot1.png)
 