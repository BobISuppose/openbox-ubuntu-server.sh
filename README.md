ubuntu-openbox-installer/
├── README.md
├── install.sh
└── scripts/
    ├── base.sh
    ├── xorg.sh
    ├── openbox.sh
    └── apps.sh


# Ubuntu Openbox Server Bootstrap

A lightweight, modular bootstrap script that turns **Ubuntu Server** into a
minimal graphical environment using **Openbox**, **tint2**, and a simple file manager.

This project is designed for:
- Homelabs
- Servers that occasionally need a local GUI
- Older or low-resource hardware
- Users who want control instead of a full desktop environment

---

## ✨ Features

- Openbox window manager (no full desktop bloat)
- tint2 panel (taskbar, tray, clock)
- PCManFM file manager + desktop icons
- NetworkManager tray applet
- Minimal dependencies
- Modular, readable shell scripts

---

## 🧱 What This Is (and Isn’t)

**This IS:**
- A minimal X11 environment
- Server-first, GUI-optional
- Easy to audit and modify

**This is NOT:**
- GNOME / KDE / XFCE
- A display manager (no login screen)
- A tiling window manager

---

## 🖥️ Supported Systems

- Ubuntu Server 20.04 LTS+
- Ubuntu Server 22.04 LTS+
- Ubuntu Server 24.04 LTS

---

## 🚀 Installation

### 1. Install Git
```bash
sudo apt update
sudo apt install -y git


git clone https://github.com/YOURUSERNAME/ubuntu-openbox-installer.git
cd ubuntu-openbox-installer

chmod +x install.sh
./install.sh

starting the GUI: startx

all logisc lives in scripts/

⚠️ Notes
	•	No display manager is installed by default
	•	You are responsible for maintaining your environment
	•	This is intentional

---

# 🧠 Refactored Scripts

## `install.sh` (entry point)

```bash
#!/bin/bash
set -e

echo "=== Ubuntu Openbox Bootstrap ==="

SCRIPT_DIR="$(cd "$(dirname "$0")" && pwd)"

bash "$SCRIPT_DIR/scripts/base.sh"
bash "$SCRIPT_DIR/scripts/xorg.sh"
bash "$SCRIPT_DIR/scripts/openbox.sh"
bash "$SCRIPT_DIR/scripts/apps.sh"

echo
echo "Installation complete."
echo "Run 'startx' to launch Openbox."

chmod +x install.sh




