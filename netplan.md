# Netplan

Traditionally some linux distros have been configuring network
interfaces in diffent ways. While debian based distros used to define
network interfaces using the package `ifupdown` and the files located
in `/etc/network`, Red Hat based distros use its own format defining
network interfaces in `/etc/sysconfig`.

Netplans is the solution proposed by Canonical and it claims to be an
agnostic network configuration system and relies on the use of other
layers called renderers. At this moment, netplan supports two
renderers:

* NetworkManager
* Systemd-networkd

[netplan.io](https://netplan.io/) is also a project supported by
Canonical and the basic configurations is a yaml file in the directory
`/etc/netplan/`:

```yaml
# This is the network config written by 'subiquity'
network:
  ethernets:
    enp1s0:
      dhcp4: true
  version: 2
```

## Useful references

* [Netplan reference](https://netplan.io/reference/)
