# LXD

[Linux containers](https://linuxcontainers.org) or LXC is the main
project providing system containers to linux and making use of both
namespaces and control groups features of the kernel.

## LXC vs LXD

LXC provides the Linux Containers userspace tools and it's available
for debian and ubuntu:

* Debian: [lxc](https://packages.debian.org/unstable/lxc)
* Ubuntu: [lxc-utils](https://packages.ubuntu.com/search?keywords=lxc-utils)

LXC commands are:

```
lxc-attach         lxc-copy           lxc-ls             lxc-unpriv-start
lxc-autostart      lxc-create         lxc-monitor        lxc-unshare
lxc-cgroup         lxc-destroy        lxc-snapshot       lxc-update-config
lxc-checkconfig    lxc-device         lxc-start          lxc-usernsexec
lxc-checkpoint     lxc-execute        lxc-stop           lxc-wait
lxc-config         lxc-freeze         lxc-unfreeze
lxc-console        lxc-info           lxc-unpriv-attach
```

LXD is an evolution of LXC, providing a daemon and a simple way for
interacting system containers with only one command: `lxc`. LXD is
available as a snap for both debian and ubuntu and it's no longer
available as a debian package.

## LXD installation

```
sudo snap install lxd
```

## Useful references

* [Getting started](https://linuxcontainers.org/lxd/getting-started-cli/)
