# morvane-niri-theme

The MorvaneOS look for niri: niri's default config with a Pastel Pink focus ring
(and border, if you turn it on) and the Twilight wallpaper.

Installs `/etc/niri/config.kdl`, which niri reads when you don't have a
`~/.config/niri/config.kdl` of your own. So until you make one, you follow package
updates. To customise, copy it to `~/.config/niri/config.kdl` and edit that.

Terminal (alacritty), bar (waybar), launcher (fuzzel) and notification (mako)
colours come from [morvane-wm-theme](https://github.com/MorvaneOS/morvane-wm-theme),
apps from [morvane-gtk-theme](https://github.com/MorvaneOS/morvane-gtk-theme). The
MorvaneOS installer installs this package with niri.

## Changing it

Edit `tools/build.py`, then run it on niri's default config (from the `niri`
package, `/usr/share/doc/niri/default-config.kdl`):

```
python tools/build.py [path/to/default-config.kdl]
```

Needs only Python. Rebuild when niri's default config changes; the build stops if
the parts it changes have moved. Commit the output, bump `pkgver`, build and publish.

## License

GPL-3.0-or-later, like niri, since the config is niri's default with the MorvaneOS
look added.
