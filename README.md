# Ansible-Role: Aminer

# Requirements

- Debian or Ubuntu

# Configuration

```
- hosts: localhost
  roles:
         - aminer
```

The following playbook can be used for development. If aminer_gitrepo is false, this role will not pull from the git repository.

```
- hosts: localhost
  vars:
    aminer_gitrepo: False
    aminer_repopath: "/home/developer/aminer"
  roles:
         - aminer

```



# Defaults
```
aminer_tools:
        - git
        - rsync
aminer_repopath: "/opt/aminer"
aminer_gitrepo: "https://git.launchpad.net/logdata-anomaly-miner"
aminer_systemdloc: "/etc/systemd/system"
aminer_vardir: "/var/lib/aminer"
aminer_user: "aminer"
aminer_group: "aminer"
```

## Defaults for Debian
```
aminer_packages:
        - python3
aminer_usershell: /usr/sbin/nologin
```


