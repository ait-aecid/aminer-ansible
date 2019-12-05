# Ansible-Role: Aminer

# Requirements

- Debian or Redhat derivats are supported

# Configuration

```
- hosts: localhost
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

## Defaults for RedHat
```
aminer_packages:
        - epel-release
        - python34
        - python36
aminer_usershell: /sbin/nologin
```
