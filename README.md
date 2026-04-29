# 8777-sway-config

This repository contains the core UI configuration files for my **Sway** environment on EndeavourOS (ThinkPad T430). It features a clean, productive setup with environment isolation for easy maintenance.

## 🛠 Key Features

* **Sway WM**: A customized tiling experience with Vim-style keybindings (`h`, `j`, `k`, `l`).
* **Waybar Isolation**: The bar configuration is isolated in `~/.config/waybar_sway/` to prevent conflicts with default system settings.
* **Integrated Clipboard**: Managed via `cliphist` and `fuzzel`, accessible via `$mod+v` or the Waybar status icon.
* **Quick Utilities**:
    * **WiFi Management**: Quick access to `nmtui` via Waybar.
    * **Wallpaper**: Integrated `waypaper` support with isolated config.
    * **Screenshots**: Area-selection screenshots using `grim` and `slurp`.

![Preview](scr.png)

## 📂 Repository Structure

* `sway/config`: Main Sway window manager settings, including gaps and custom keybindings.
* `waybar_sway/config.jsonc`: Module layout for the status bar, including CPU, memory, and battery indicators.
* `waybar_sway/style.css`: Visual styling for Waybar, featuring a dark Tokyo Night-inspired aesthetic.

## 🚀 Installation & Usage

1. **Dependencies**: Ensure you have `sway`, `waybar`, `fuzzel`, `cliphist`, `wl-clipboard`, `waypaper`, and `nmtui` installed.
2. **Placement**:
    * Place the `sway` config in `~/.config/sway/config`.
    * Place the `waybar_sway` folder in `~/.config/waybar_sway/`.
3. **Launch**: The Sway config is set to automatically kill existing Waybar instances and launch with the specific isolated paths:
    ```bash
    waybar -c ~/.config/waybar_sway/config.jsonc -s ~/.config/waybar_sway/style.css
    ```

## ⚖️ License & Acknowledgements

* **Waybar Configuration**: The base logic for the Waybar modules is a modified version of the [sway-dotfiles](https://github.com/Ruixi-rebirth/sway-dotfiles) by **Ruixi-rebirth**.
* **License Notice**: As the original work is licensed under **GPL-3.0**, my modifications to the Waybar configuration in this repository are also distributed under the **GPL-3.0 License** to remain compliant with the copyleft requirements.
* **Other Files**: The Sway configuration and custom scripts are provided as-is for personal use.

---

### 💡 A Note on the GPL-3.0 Credit
Since **Ruixi-rebirth** uses GPL-3.0, you are legally required to keep the same license for the *Waybar* part of your project if you distribute it. I've added a specific "License Notice" in the README to make sure you are covered. Using **LazyGit** to push this README will make your repo look very professional!
