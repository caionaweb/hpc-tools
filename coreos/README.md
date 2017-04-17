# Basic installation of CoreOS

**Obs.: Because it's a distro for containers, by default Docker is installed**

**Download Image and boot**

https://coreos.com/os/docs/latest/booting-with-iso.html


**Create a password hash** 


```
sudo openssl passwd -1
```

**Create cloud_config.yml with template **

```
#cloud-config
users:
- name: USER
  passwd: PASS_HASH
  groups:
  - sudo
  - docker

```

**Run instalattion**

```
sudo coreos-install -d /dev/sda -C stable -c cloud_config.yml
```

**Wait and reboot.**

**Done.**