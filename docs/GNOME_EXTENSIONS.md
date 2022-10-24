# Role: theliomcfly.workstation.gnome_extensions

# Description

This role allows edits dconf settings.

# Requirements

Outside of the ansible.builtin collecitons this collection requires the ```community.general``` collection to be installed.

### Install the collection ```community.general``` if not already
```
ansible-galaxy collectin install community.general
```

### Install psutils if not already (Optional)

This step is optional since the ```theliomcfly.workstation.gnome_settings``` role ensures that it's installed.`

#### Fedora
```
sudo dnf install python3-psutil
```

# Role variables 

**```gnome_extensions```** (list of dictionaries): This is a list of dictionaries. Each key below is described below

## ```gnome_extensions``` Dictionary Values

**```gnome_user```** (optional) - The user that the extension should be installed for

**```extension_ids```** (required list) - List of extension IDs to install from extensions.gnome.org. The ID can be found from the URL for the extension.
(E.g.) The ID is 2986 in URL https://extensions.gnome.org/extension/2986/runcat/
