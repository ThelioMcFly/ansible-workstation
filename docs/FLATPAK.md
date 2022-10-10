# Role: theliomcfly.workstation.flatpak

# Description

his role will ensure flatpak is installed, configure the flathub repo, and install the specified flatpaks. Since some distributions filter the repoistory from [flathub.org](https://flathub.org/home) to curate the selection from Gnome Software we create a remote repository that is unfiltered for the user's convenience.

# Role variables and their default values

The ```flatpak_required_packages``` variable is a list of the packages to install flatpak from the ditro repositories.

**```flatpak_required_packages```** (list): Default => ```['flatpak', 'flatpak-libs', 'flatpak-selinux', 'flatpak-session-helper' ]```

The ```flatpak_required_apps``` is a list of dictionaries that contain the name of the flatpak to install, the state (```present``` or ```absent```), method (```user``` or ```system```), and the remote flatpak repository.

**```flatpak_required_apps```** (list of dictionaries): Default => ```undefined```

The dictionaries ```flatpak_required_apps``` expect have the keys as follows:
- **```name```** (string): The fully qualified name of the app to install (e.g. ```com.valvesoftware.Steam```)
- **```state```** (string): Either ```present``` (default) or ```absent```
- **```method```** (string): Either ```user``` (default) or ```system```
- **```remote```** (string): The name of the flatpak repository to use - Default => ```unfiltered-flathub``` (created by this role)