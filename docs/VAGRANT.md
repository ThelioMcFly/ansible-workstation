# Role: theliomcfly.workstation.vagrant

# Description

This role allows edits dconf settings.

# Role variables and their default values

**```vargrant_required_packages```** (list): List of required packages to install. Default => ['vagrant', 'vagrant-libvirt']```

**```libssh_package```** (string): The name of the libssh package to install. This is needed to get the vagrant-libvirt provider to work properly with newer Vagrant boxes. Default => ```libssh```

**```krb5libs_package```** (string): The name of the krb5 library package. This is needed to get the vagrant-libvirt provider to work properly with newer Vagrant boxes. Default => ```krb5-libs```