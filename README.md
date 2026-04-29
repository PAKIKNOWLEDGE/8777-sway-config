---

# 8777-sway-config

This repository contains the core UI configuration files for my **Sway** environment on EndeavourOS (ThinkPad T430). [cite_start]It features a clean, productive setup with environment isolation for easy maintenance[cite: 6].

## 🛠 Key Features

* [cite_start]**Sway WM**: A customized tiling experience with Vim-style keybindings (`h`, `j`, `k`, `l`)[cite: 6, 9, 10].
* [cite_start]**Waybar Isolation**: The bar configuration is isolated in `~/.config/waybar_sway/` to prevent conflicts with default system settings[cite: 6].
* [cite_start]**Integrated Clipboard**: Managed via `cliphist` and `fuzzel`, accessible via `$mod+v` or the Waybar status icon[cite: 5, 9].
* **Quick Utilities**:
    * [cite_start]**WiFi Management**: Quick access to `nmtui` via Waybar[cite: 4].
    * [cite_start]**Wallpaper**: Integrated `waypaper` support with isolated config[cite: 6, 8].
    * [cite_start]**Screenshots**: Area-selection screenshots using `grim` and `slurp`[cite: 15].
![](scr.png)
## 📂 Repository Structure

* [cite_start]`sway/config`: Main Sway window manager settings, including gaps and custom keybindings[cite: 6, 15].
* [cite_start]`waybar_sway/config.jsonc`: Module layout for the status bar, including CPU, memory, and battery indicators[cite: 1, 3, 5].
* `waybar_sway/style.css`: Visual styling for Waybar, featuring a dark Tokyo Night-inspired aesthetic.

## 🚀 Installation & Usage

1.  **Dependencies**: Ensure you have `sway`, `waybar`, `fuzzel`, `cliphist`, `wl-clipboard`, `waypaper`, and `nmtui` installed.
2.  **Placement**:
    * Place the `sway` config in `~/.config/sway/config`.
    * Place the `waybar_sway` folder in `~/.config/waybar_sway/`.
3.  [cite_start]**Launch**: The Sway config is set to automatically kill existing Waybar instances and launch with the specific isolated paths[cite: 6]:
    ```bash
    waybar -c ~/.config/waybar_sway/config.jsonc -s ~/.config/waybar_sway/style.css
    ```

## ⚖️ License & Acknowledgements

* **Waybar Configuration**: The base logic for the Waybar modules is a modified version of the [sway-dotfiles](https://github.com/Ruixi-rebirth/sway-dotfiles) by **Ruixi-rebirth**.
* **License Notice**: As the original work is licensed under **GPL-3.0**, my modifications to the Waybar configuration in this repository are also distributed under the **GPL-3.0 License** to remain compliant with the copyleft requirements.
* **Other Files**: The Sway configuration and custom scripts are provided as-is for personal use.

---

### 💡 A Note on the GPL-3.0 Credit
Since **Ruixi-rebirth** uses GPL-3.0, you are legally required to keep the same license for the *Waybar* part of your project if you distribute it. I've added a specific "License Notice" in the README to make sure you are covered. [cite_start]Using **LazyGit** to push this README will make your repo look very professional! [cite: 6]
