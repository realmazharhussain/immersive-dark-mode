# Immersive Dark Mode (for GNOME only)

Changes gtk3/legacy applications, icon and cursor theme when dark mode is enabled/disabled.

## Install

### System-wide

1. Copy `immersive-dark-mode` to `/usr/bin/`
2. Copy `immersive-dark-mode.desktop` to `/etc/xdg/autostart/`

### For Single User

1. Copy `immersive-dark-mode` to `$HOME/.local/usr/bin/`
2. Copy `immersive-dark-mode.desktop` to `$HOME/.config/autostart/`

## Run/Execute

After installation, the tool will run automotically on the next boot. To run it without
having to reboot, just open a terminal and run the command `immersive-dark-mode & disown`.


## Customize

By default, Adwaita is used as the GTK3 theme and Breeze as the cursor theme. To change
the values, edit `immersive-dark-mode` file itself. It is not difficult.
