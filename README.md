# 8777-sway-config

This repository contains the core UI configuration files for my **Sway** environment on EndeavourOS (ThinkPad T430). It features a clean, productive setup with environment isolation for easy maintenance.

## 🛠 Key Features

* [cite_start]**Sway WM**: A customized tiling experience with Vim-style keybindings (`h`, `j`, `k`, `l`)[cite: 6].
* [cite_start]**Waybar Isolation**: The bar configuration is isolated in `~/.config/waybar_sway/` to prevent conflicts with default system settings[cite: 6].
* [cite_start]**Integrated Clipboard**: Managed via `cliphist` and `fuzzel`, accessible via `$mod+v` or the Waybar status icon[cite: 5, 9].
* **Quick Utilities**:
    * [cite_start]**WiFi Management**: Quick access to `nmtui` via Waybar[cite: 4].
    * [cite_start]**Wallpaper**: Integrated `waypaper` support with isolated config[cite: 6, 8].
    * [cite_start]**Screenshots**: Area-selection screenshots using `grim` and `slurp`[cite: 15].

![Preview](scr.png)

## ⚠️ Dependencies & Hardcoded Paths (Important)

Please note that this configuration contains several **hardcoded** settings. Ensure the following specific software is installed, or modify `sway/config` to match your environment:

1. **Terminal**: Defaulted to `kitty`. [cite_start]To change this, modify the `set $term kitty` line[cite: 6].
2. **Launcher**: Defaulted to `fuzzel`. [cite_start]To change this, modify the `set $menu fuzzel` line[cite: 6].
3. **Environment Isolation**: 
    * [cite_start]Multiple paths reference `~/.config/waybar_sway/` and `~/.config/waypaper_sway/`[cite: 6].
    * The **WiFi Management** module is hardcoded to launch `kitty -e nmtui`. [cite_start]If you use a different terminal, update the `on-click` command in `waybar_sway/config.jsonc`[cite: 4].
4. **Fonts**: The UI relies on `Sarasa UI SC Nerd Font` and `Noto Color Emoji` for proper icon and text rendering.

## 📂 Repository Structure

* [cite_start]`sway/config`: Main Sway window manager settings, including gaps and custom keybindings[cite: 6, 15].
* [cite_start]`waybar_sway/config.jsonc`: Module layout for the status bar, including CPU, memory, and battery indicators[cite: 1, 3, 5].
* `waybar_sway/style.css`: Visual styling for Waybar, featuring a dark Tokyo Night-inspired aesthetic.

## 🚀 Installation & Usage

1. **Placement**:
    * Place the `sway` config file in `~/.config/sway/config`.
    * Place the `waybar_sway` folder in `~/.config/waybar_sway/`.
2. [cite_start]**Launch**: The Sway config is set to automatically reload and launch Waybar with the specific isolated paths[cite: 6]:
    ```bash
    waybar -c ~/.config/waybar_sway/config.jsonc -s ~/.config/waybar_sway/style.css
    ```

## ⚖️ License & Acknowledgements

* **Waybar Configuration**: The base logic for the Waybar modules is a modified version of the [sway-dotfiles](https://github.com/Ruixi-rebirth/sway-dotfiles) by **Ruixi-rebirth**.
* **License Notice**: As the original work is licensed under **GPL-3.0**, my modifications to the Waybar configuration in this repository are also distributed under the **GPL-3.0 License** to remain compliant with copyleft requirements.
* **Other Files**: The Sway configuration and custom scripts are provided as-is for personal use.
