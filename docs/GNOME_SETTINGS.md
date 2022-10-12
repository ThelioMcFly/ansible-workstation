# Role: theliomcfly.workstation.gnome_settings

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

# Role variables and their default values

**```config```** (list of dictionaries): This is a list of dictionaries. Each key below is described below

**```dconf_user```** (string): The user that will get the setting specified. Default => ```remote_user``` (the user used to connect to the host)

**```key```** (string): The dconf key that is being set. This has to be in the GVariant format and **must** start with a slash (e.g. "org/gnome/desktop/interface/color-scheme" )

**```value```** (string): The value of the dconf setting. 

**```state```** (string): Whether the string should be ```present``` or ```absent```

