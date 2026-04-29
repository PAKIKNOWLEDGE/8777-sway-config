8777-sway-config
[](scr.png)

This repository contains the core UI configuration files for my Sway environment on EndeavourOS (ThinkPad T430). It features a clean, productive setup with environment isolation for easy maintenance.
🛠 Key Features

* Sway WM: A customized tiling experience with Vim-style keybindings (h, j, k, l). * Waybar Isolation: The bar configuration is isolated in ~/.config/waybar_sway/ to prevent conflicts with default system settings. * Integrated Clipboard: Managed via cliphist and fuzzel, accessible via $mod+v or the Waybar status icon.   

    Quick Utilities:
    * WiFi Management: Quick access to nmtui via Waybar. * Wallpaper: Integrated waypaper support with isolated config. * Screenshots: Area-selection screenshots using grim and slurp.   

⚠️ Dependencies & Hardcoded Paths (Important)

Please note that this configuration contains several hardcoded settings. Ensure the following specific software is installed, or modify sway/config to match your environment:

    Terminal: Defaulted to kitty. To change this, modify the set $term kitty line.   

Launcher: Defaulted to fuzzel. To change this, modify the set $menu fuzzel line.   

Environment Isolation:
* Multiple paths reference ~/.config/waybar_sway/ and ~/.config/waypaper_sway/.   

    The WiFi Management module is hardcoded to launch kitty -e nmtui. If you use a different terminal, update the on-click command in waybar_sway/config.jsonc.   

    Fonts: The UI relies on Sarasa UI SC Nerd Font and Noto Color Emoji for proper icon and text rendering.

📂 Repository Structure

* sway/config: Main Sway window manager settings, including gaps and custom keybindings. * waybar_sway/config.jsonc: Module layout for the status bar, including CPU, memory, and battery indicators.   

    waybar_sway/style.css: Visual styling for Waybar, featuring a dark Tokyo Night-inspired aesthetic.

🚀 Installation & Usage

    Placement:

        Place the sway config file in ~/.config/sway/config.

        Place the waybar_sway folder in ~/.config/waybar_sway/.
        2. Launch: The Sway config is set to automatically reload and launch Waybar with the specific isolated paths:   

Bash

    waybar -c ~/.config/waybar_sway/config.jsonc -s ~/.config/waybar_sway/style.css

⚖️ License & Acknowledgements

    Waybar Configuration: The base logic for the Waybar modules is a modified version of the sway-dotfiles by Ruixi-rebirth.

    License Notice: As the original work is licensed under GPL-3.0, my modifications to the Waybar configuration in this repository are also distributed under the GPL-3.0 License to remain compliant with copyleft requirements.

    Other Files: The Sway configuration and custom scripts are provided as-is for personal use.
