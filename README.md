<p align="center">
  <img src="https://hyprland.org/img/logo.svg" width="80" />
</p>

<h1 align="center">hyprkit</h1>

<p align="center">
  <b>A collection of scripts and utilities for Hyprland desktops</b>
</p>

<p align="center">
  <a href="#tools">Tools</a> &bull;
  <a href="#install">Install</a> &bull;
  <a href="#dependencies">Dependencies</a>
</p>

---

## Tools

### `theme-switch`

Visual wallpaper picker with system-wide color scheme generation. Picks a wallpaper, extracts a color palette using [matugen](https://github.com/InioX/matugen), and propagates it everywhere.

```
theme-switch              # rofi visual picker
theme-switch <path>       # apply specific wallpaper
theme-switch --random     # random wallpaper
```

**What it touches:**
- Wallpaper via `swww` with a circle-reveal animation from cursor position
- Hyprland window borders and shadows
- HyprPanel bar and menu colors
- Kitty terminal colors
- GTK 3/4 theme variables
- GNOME accent color

<details>
<summary>Screenshot</summary>
<br>
<i>Coming soon</i>
</details>

---

## Install

```bash
git clone git@github.com:z89/hyprkit.git ~/.config/hyprkit

# symlink tools into PATH
ln -s ~/.config/hyprkit/theme-switch/theme-switch ~/.local/bin/theme-switch
```

Bind it in your `hyprland.conf`:
```
bind = $mainMod SHIFT, W, exec, theme-switch
```

## Dependencies

| Package | Purpose |
|---------|---------|
| `matugen` | Color scheme extraction from wallpaper |
| `swww` | Animated wallpaper daemon |
| `rofi-wayland` | Visual picker UI |
| `hyprpanel` | Bar (optional, auto-detected) |
| `python3` | Accent color mapping |
| `kitty` | Terminal (optional, auto-detected) |

## License

MIT
