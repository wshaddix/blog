---
title: Workstation Setup
order: 100
nextprev:
  mode: hide
---

## Operating System Setup

## Desktop

You are going to be looking at your desktop a lot, so pick a background that brings you happiness. Every time you look at it you should feel joy and excitement. I use the following background that I found from <https://www.youtube.com/@typecraft_dev>
![Wallpaper](/static/img/wallpaper.jpeg)

## Git

### Installation

```bash
yay -S git
```

### Configuration

### Aliases

## Terminal

### Install a Nerd Font

```bash
yay -S otf-sfmono-patched
```

### Install WezTerm Terminal

```bash
yay -S wezterm
```

### Configure WezTerm Terminal

```lua
local wezterm = require("wezterm")
local config = wezterm.config_builder()
local act = wezterm.action

-- Fonts
config.font_size = 15
config.line_height = 1.2
config.font = wezterm.font("SF Mono Powerline")

-- Colors
config.color_scheme = "Catppuccin Mocha"
config.colors = {
 cursor_bg = "#7aa2f7",
 cursor_border = "#7aa2f7",
}

-- Tabs
config.use_fancy_tab_bar = false
config.tab_max_width = 32
config.show_new_tab_button_in_tab_bar = false

config.keys = {
 {
  key = "E",
  mods = "CTRL|SHIFT",
  action = act.PromptInputLine({
   description = "Enter new name for tab",
   action = wezterm.action_callback(function(window, pane, line)
    -- line will be `nil` if they hit escape without entering anything
    -- An empty string if they just hit enter
    -- Or the actual line of text they wrote
    if line then
     window:active_tab():set_title(line)
    end
   end),
  }),
 },
}

return config
```

### Install Starship

```bash
curl -sS https://starship.rs/install.sh | sh
```
