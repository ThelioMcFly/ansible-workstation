# Role: theliomcfly.workstation.browser

# Description:
This role will install the perferred browser. All ```brave_repo_*``` variables mirror the ```ansible.builtin.yum_repository``` module.

# Role variables and their default values

**```browser_install_brave```** (boolean): Default => ```yes```

**```brave_repo_name```** (string): Default => ```brave-browser``` 

**```brave_repo_description```** (string): Default => ```brave-browser```

**```brave_repo_url```** (string): Default => ```https://brave-browser-rpm-release.s3.brave.com/x86_64/```

**```brave_repo_enabled```** (boolean): Default => ```yes```

**```brave_repo_gpgkey```** (string): Default => ```https://brave-browser-rpm-release.s3.brave.com/brave-core.asc```

**```brave_package_list```** (list): Default => ```['brave-browser']```


# Example playbook usage
```
- name: Setup required environment
  hosts: all
    
  roles:
  - role: theliomcfly.workstation.browser
      tags: browser
      become: true
```