# ThelioMcFly's Workstation collection

# Description:
This colleciton was created to bring a fresh Fedora install from installed to configured as needed. Eventually other distros will be supported (e.g. Pop!_OS)

# Supported (tested) Linux Distributions
- [x] Fedora 36

# Requirements

## Install the required collections

Outside of the ansible.builtin collecitons this collection requires the ```community.general``` collection to be installed.

### Install the collection ```community.general``` if not already
```
ansible-galaxy collectin install community.general
```

### Install psutils if not already 

This step is optional since the ```theliomcfly.workstation.gnome_settings``` role ensures that it's installed.`

### Fedora
```
sudo dnf install python3-psutil
```

# Install the collection
```
ansible-galaxy collection install theliomcfly.workstation
```

# Roles in this collection

- [Browser](docs/BROWSER.md) - This role will install browsers on the workstation
- [Flatpak](docs/FLATPAK.md) - This role will ensure flatpak is installed, configure the flathub repo, and install the specified flatpaks.