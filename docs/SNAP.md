# Role: theliomcfly.workstation.snap

# Requirements

## Install the required collections

Outside of the ansible.builtin collecitons this collection requires the ```community.general``` collection to be installed.

### Install the collection ```community.general``` if not already
```
ansible-galaxy collectin install community.general
```

# Role variables and their default values

**```snap_required_packages```** (list): List of required packages for a working snap installation. Default => ```snapd```

**```snap_install_list```** (list): An optional list of snaps to install on the system. 