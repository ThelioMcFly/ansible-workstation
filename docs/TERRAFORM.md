# Role: theliomcfly.workstation.snap

# Requirements

## Install the required collections

Outside of the ansible.builtin collecitons this collection requires the ```community.general``` collection to be installed.

### Install the collection ```community.general``` if not already
```
ansible-galaxy collectin install community.general
```

# Role variables and their default values

**```terraform_required_dep_packages```** (list): List of dependencies before terraform can be installed. Default => ```['dnf-plugins-core']```

**```terraform_required_repo```** (string): The URL of the terraform repo to be installed. Default => ```https://rpm.releases.hashicorp.com/fedora/hashicorp.repo```