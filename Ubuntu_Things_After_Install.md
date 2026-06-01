# Things do after install Ubuntu 26.04 | Documentation Guideline | Hoang Do

After installing Ubuntu 26.04, the desktop is ready to use, but a few setup steps make the system easier to work with day to day. Updating packages, checking drivers, installing media codecs, setting up backups, and reviewing privacy settings are good first tasks on a new installation.

This guide explains what to do after installing Ubuntu 26.04. The checklist is aimed at desktop users who want a clean, practical setup without adding unnecessary tools.

---

## 1. Update Ubuntu
Update package lists and installed packages

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get autoremove
```

## 2. Install Media Codecs
Ubuntu does not include every media codec by default. If you want better support for common audio and video files, Microsoft fonts, and some archive formats, install the restricted extras package:

```bash
sudo apt-get install ubuntu-restricted-extras
```

## 3. Install Essential Utilities
Enhance your system by grabbing the best tools for configuration and monitoring:
* GNOME Tweaks: Allows you to modify fonts, window behaviors, and themes.
* Extension Manager: Lets you customize the look of the GNOME 50 desktop (e.g., adding desktop cubes or moving the dock).

```bash
sudo apt-get install gnome-tweaks gnome-shell-extension-manager -y
```

## 4. Enable Flatpak and Flathub
Ubuntu includes Snap support by default, and many applications are available from the Ubuntu App Center. Flatpak is another popular desktop app format, and Flathub provides current builds of many Linux desktop applications.

Install Flatpak and the GNOME Software plugin:

```bash
sudo apt-get install flatpak gnome-software-plugin-flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

## 5. Enable the Firewall
Ubuntu ships with a firewall utility (UFW) that is disabled by default. Turn it on immediately to block unsolicited inbound connections:

```bash
sudo ufw enable
```
## 6. Install Essential Development Tools

Even if you are not a full-time developer, many administration scripts and third-party tools require a working build environment. 

```bash
sudo apt-get install -y \
    build-essential \
    git \
    curl \
    wget \
    python3-pip \
    python3-venv \
    ca-certificates \
    btop \
    fastfetch \
    openjdk-25-jdk \
    maven \
    ant
```

You should also setup IDE such as: VS Code, Eclipse, etc

## 7. GNOME Extensions
| Extensions | Description |
| :--- | :--- |
| **Blur my Shell** | Adds a modern, frosted glass blur effect to different parts of the GNOME Shell, including the top panel, dash, and application overview background. |
| **Compiz alike magic lamp effect** | Mimics the classic Linux "Magic Lamp" (Genie) window minimization animation, smoothly curving your windows down into the dock. |
| **Compiz windows effect** | Brings back nostalgic desktop effects from the old Compiz window manager, most notably the famous "wobbly windows" physics engine when dragging applications. |
| **Coverflow Alt-Tab** | Replaces the default, flat window switcher with a 3D "Cover Flow" style layout, letting you flip through active application windows in a carousel preview. |
| **Dash2Dock Animated** | Enhances the standard Dash to Dock modification by adding smooth, customized animations and physics when the app dock hides, reveals, or launches items. |
| **Tiling Shell** | Introduces advanced, Windows 11-style window snapping and custom grid layouts to GNOME, giving you powerful window management without needing a full tiling window manager. |
| **User Themes** | A fundamental customization extension that unlocks the ability to load custom shell themes directly from your user directory (`~/.themes`). |
| **Vitals** | Integrates a data-rich monitor into your top menu bar, displaying real-time system stats like CPU temperature, fan speed, memory usage, and network speed. |

