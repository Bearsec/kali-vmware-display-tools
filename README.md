# Kali VMware Display Tools

A small collection of utilities for improving display resolution management in **Kali Linux running inside VMware Fusion**.

These tools provide quick access to optimal screen settings depending on the current window size, and improve usability in HiDPI environments.

## 🖥 What's included

| File                                | Purpose |
|-------------------------------------|---------|
| `set-recommended-resolution`        | Bash script that selects and applies the display resolution marked as "recommended" (`+`) by `xrandr`. Useful when VMware Fusion dynamically resizes the guest window. |
| `auto-adjust-resolution.desktop`    | XFCE desktop launcher for quickly applying the recommended resolution via the script above. |
| `kali-hidpi-mode.desktop`           | Official Kali shortcut for toggling HiDPI desktop scaling. |
| `xfce-display-settings.desktop`     | Shortcut to open XFCE display settings directly from the desktop. |

## 📦 Installation

1. Clone the repository:

```bash
git clone https://github.com/Bearsec/kali-vmware-display-tools.git
```

2. Copy files to the desktop:

```bash
cp kali-vmware-display-tools/*.desktop ~/Desktop
sudo cp kali-vmware-display-tools/set-recommended-resolution /usr/bin/
sudo chmod +x /usr/bin/set-recommended-resolution
```

3. Make desktop launchers executable:

```bash
chmod +x ~/Desktop/*.desktop
```

4. (Optional) Reload the desktop:

```bash
xfdesktop --reload
```

## 🧠 Notes

- The `set-recommended-resolution` script uses `xrandr` to detect and apply the resolution marked with `+`, which is typically managed by VMware Tools.
- Place these `.desktop` launchers on the desktop for one-click access.
- Designed for XFCE in Kali; may require tweaks in other environments.

## 📽 Demo

[![Display Tools Demo](assets/demo.gif)](https://github.com/Bearsec/kali-vmware-display-tools)


