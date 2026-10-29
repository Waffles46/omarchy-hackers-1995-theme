# Optional app profiles

The base theme uses Omarchy's supported data files. These personal app customizations are separate and never run automatically during theme installation.

## Strata

Install Strata separately. Save the following as `~/.config/strata/themes/hackers-1995.toml`:

```toml
name = "Hackers 1995"
background = "#000000"
surface = "#000000"
text = "#00ff41"
accent = "#00ff41"
danger = "#ff3131"
muted = "#111111"
highlight = "#003b10"
border = "#008f11"
dim_text = "#008f11"
```

Merge these two keys into the existing `~/.config/strata/settings.toml`, retaining the other settings:

```toml
mode = "theme"
theme = "hackers-1995"
```

This is the palette used by the personal Strata profile. Window transparency comes from the user's compositor configuration; it is not supplied by this theme.

## Foot and transparency

Omarchy generates Foot's colors from `colors.toml`. The captured Foot windows use the author's live terminal background alpha of `0.97`, plus compositor opacity of `0.83` when focused and `0.77` when unfocused. Strata uses compositor opacity of `0.79`. The preview adds no darker overlay and supplies no opacity override. Wallpaper brightness and which window has focus affect the visible result. These are personal settings, not necessary for the theme to work, and are not applied by this repository.

The same distinction applies to the custom taskbar, title bars, font size, wallpaper fit, and the arrangement of applications in the screenshot.

## Neovim

A community theme's Lua files are discarded by Omarchy's installed-theme rules. The base installation therefore uses Omarchy's generated editor theme from `colors.toml`.

The author's local editor uses a separate Tokyo Night override that follows the same green palette. That editor configuration is not required by the release and is not automatically installed. The preview may show the optional personal editor configuration; it does not promise identical syntax highlighting on a fresh installation.

## Signal

Signal's personal green appearance uses a separately patched, user-owned Signal runtime. It is specific to Signal's packaged application version and is not a standard Omarchy theme feature.

This release does not patch Signal, copy a Signal profile, or distribute a modified Signal application. Its desktop palette can be used as a color reference for a separately maintained Signal customization.

## Spotify Terminal

The author's Spotify Terminal is a separate custom application with its own green curses palette, private desktop backend, and bridge. It is not bundled here and is not required by the theme.

That application reserves terminal palette entries 10–14 for green, muted green, amber, yellow, and red. Omarchy's live terminal recoloring can overwrite those entries. The author's machine has a separate theme-change hook that restores them only in the Spotify terminal window.

Do not apply that palette workaround to ordinary terminals: those slots also have standard ANSI meanings. This theme does not change another user's Spotify application or install the author's backend, bridge configuration, or hook.
