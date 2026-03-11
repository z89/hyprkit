<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/z89/hyprkit/main/assets/logo-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/z89/hyprkit/main/assets/logo-light.svg">
    <img src="https://raw.githubusercontent.com/z89/hyprkit/main/assets/logo-dark.svg" width="520" alt="hyprkit" />
  </picture>
</p>

<p align="center">
  <code>scripts and utilities for Hyprland desktops</code>
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
- Kitty terminal colors (smooth fade transition)
- GTK 3/4 theme variables
- GNOME accent color

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
