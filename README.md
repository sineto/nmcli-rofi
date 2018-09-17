# nmcli-rofi

A simple manager for network connections using [rofi](https://github.com/DaveDavenport/rofi) and 
[nmcli](https://jlk.fjfi.cvut.cz/arch/manpages/man/nmcli.1). 
Strongly inspired/based on [rofi-wifi-menu](https://github.com/zbaylin/rofi-wifi-menu). 
Most of the code (I would say all code) was copied from the original creator. 
I've only refactored the code to improve performance and easily add new features.

## Features
* Disable/Enable device
* Connect to existing network
* Disconnect from active networking
* Requests password
* Manual Connections
  * Resquest SSID and Password of the network
* External source config

## Requirements
* NetworkManager (nmcli)
* Rofi
* wireless_tools

## Usage
### To use with click event on polybar
```
[module/network]
type = internal/network
...
format-connected = %{A1:$HOME/.config/polybar/scripts/nmcli-rofi:}<ramp-signal>%{A}
format-disconnected = %{A1:$HOME/.config/polybar/scripts/nmcli-rofi:}icon-or-label%{A}
...
```

### To use with i3wm keybinding
```
bindsym $mod+n exec /path/to/nmcli-rofi
```
Replace modifier if you need
