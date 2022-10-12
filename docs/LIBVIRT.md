# Role: theliomcfly.workstation.gnome_settings

# Description

This role allows edits dconf settings.

# Role variables and their default values

**```libvirt_required_packages```** (list) - This is the list of packages needed for a functioning libvirt install. Default =>
```
libvirt
libvirt-daemon
libvirt-client
libvirt-devel
virt-install
virt-manager
qemu-kvm
bridge-utils
libguestfs-tools
guestfs-tools
virt-top
```

**```libvirt_service```** (string): The name of the libvirt service to start. Default => ```libvirtd.service```

**```libvirt_use_legacy```** (boolean): Newer versions of libvirt has switched to modular services instead of a monolithic service. This tells the role whether or not to use the legacy monolithic service or newer modular services. Default => ```false```

**```libvirt_legacy_services```** (list): List of legacy systemd units to ensure are started. Default =>
```
libvirtd.service
libvirtd.socket
libvirtd-ro.socket
libvirtd-admin.socket
libvirtd-tcp.socket
libvirtd-tls.socket
```

**```libvirt_required_services```** (list): List of modular systemd units to ensure are started. Default =>
```
virtqemud.socket
virtqemud-ro.socket
virtqemud-admin.socket
virtinterfaced.socket
virtinterfaced-ro.socket
virtinterfaced-admin.socket
virtnetworkd.socket
virtnetworkd-ro.socket
virtnetworkd-admin.socket
virtnodedevd.socket
virtnodedevd-ro.socket
virtnodedevd-admin.socket
virtnwfilterd.socket
virtnwfilterd-ro.socket
virtnwfilterd-admin.socket
virtsecretd.socket
virtsecretd-ro.socket
virtsecretd-admin.socket
virtstoraged.socket
virtstoraged-ro.socket
virtstoraged-admin.socket
```