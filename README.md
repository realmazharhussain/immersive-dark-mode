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

The default behavior is to use 'Adwaita' and 'Adwaita-dark' for GTK3 and keep icon and
cursor themes untouched. To change this behavior, edit `immersive-dark-mode` file to
your liking. It is very easy to do and specific instructions are given below.

### Change GTK3/Legacy Application Themes

Edit `immersive-dark-mode` file and simply replace 'Adwaita' and 'Adwaita-dark' with
names of whatever themes you like.

### Change Icon & Cursor Themes

Edit `immersive-dark-mode` file, uncomment the relevant lines and simply replace
default values with names of whatever themes you like.

### Example

For example, to change cursor theme to 'Breeze' (dark) and 'Breeze\_Snow' (light), edit
`immersive-dark-mode` file as follows

```diff
 def re_set_theme(*args):
     if settings['color-scheme'] != 'prefer-dark':
-        #settings['cursor-theme'] = 'Adwaita'
+        settings['cursor-theme'] = 'Breeze_Snow'
         #settings['icon-theme'] = 'Adwaita'
         settings['gtk-theme'] = 'Adwaita'       # GTK3 Theme
         #gtk_css.unlink(missing_ok=True)        # GTK4 Theme Support
         #gtk_css.symlink_to(light_css)          # GTK4 Theme Support

     else:
-        #settings['cursor-theme'] = 'Adwaita'
+        settings['cursor-theme'] = 'Breeze'
         #settings['icon-theme'] = 'Adwaita'
         settings['gtk-theme'] = 'Adwaita-dark'  # GTK3 Theme
         #gtk_css.unlink(missing_ok=True)        # GTK4 Theme Support
         #gtk_css.symlink_to(dark_css)           # GTK4 Theme Support

```
