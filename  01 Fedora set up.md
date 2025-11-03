# Fedora 42 Server Configuration (Netadmin Infrastructure)

This document outlines the core commands used to set up the Fedora 42 server environment, covering the Xfce desktop, system administration, networking, firewall, and DHCP services.

## 1. Graphical Environment Setup (Xfce Desktop)

These commands install the required graphical components and configure the system to boot into the graphical login manager (XDM).

| Command | Description |
| :--- | :--- |
| `sudo dnf install @base-x` | [cite_start]Installs the core X server packages and dependencies. [cite: 90] |
| `sudo dnf install @xfce-desktop` | [cite_start]Installs the full Xfce desktop environment group. [cite: 91] |
| `sudo systemctl enable xdm.service` | [cite_start]Enables the XDM login manager to start at boot. [cite: 92] |
| `sudo systemctl set-default graphical.target` | [cite_start]Switches the default boot mode from text (multi-user) to GUI (graphical). [cite: 92] |
| `sudo reboot` | [cite_start]Applies the changes and starts the server into the new graphical login screen (XDM). [cite: 93] |

**Quick GUI Switch:**

```bash
[cite_start]sudo systemctl isolate graphical.target  # Temporarily switches to GUI mode. [cite: 94]
