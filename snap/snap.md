# Snap

Snap is a Canonical supported project to provide dependency free
applications and it's mainly used when an application is not correctly
supported by the package management system (APT). There are some
typical cases when an application is not correctly supported by the
package management system, including the latest releases or non-free
applications.

Snap provides dependency free applications providing static compiled
binaries or packages including all the dynamic dependencies. Snap
packages are independent to each others but in general are bigger and
slower than those provided by the package management system. Snap
packages are not a good general solution to provide all the software
of a system but can be a good option for specific cases.

Another well-known utility for dependecy free package management in
linux is [Flatpak](https://www.flatpak.org/), formerly known as
xdg-app.

## Snap components

* snap is both the command line interface and the application package
  format
* snapd is the service that manages and maintains the snaps
* snapcraft is the command and the framework used to build snaps
* [Snap Store](https://snapcraft.io/store) provides a place to upload
  snaps, and for users to browse and install

The project is called [snapcraft](https://snapcraft.io/), is supported
by Canonical and the repositories are available on
[Github](https://github.com/snapcore/)

## Snapd debian package

Snap must be initially installed as a debian package with the package
management system. The package is called snapd and it includes both
the daemon that and the snap CLI. Once installed snap can be updated
by snap itself with `snap refresh snapd`

## Using snap

* List installed snaps

```
$ snap list
Name          Version                  Rev    Tracking       Publisher   Notes
core18        20220309                 2344   latest/stable  canonical✓  base
core20        20220329                 1434   latest/stable  canonical✓  base
juju          2.9.29                   18965  latest/stable  canonical✓  classic
...
```

* Find out snaps in Snap Store

```
$ snap find gimp
Name                    Version  Publisher        Notes  Summary
gimp                    2.10.28  snapcrafters     -      GNU Image Manipulation Program
gutenprint-printer-app  1.0      openprinting✓    -      Gutenprint Printer Application
photogimp               2.10.20  pedro.ermarinho  -      Patch para o GIMP
...
```

Snaps binaries are installed on the directory `/snaps/bin/`. The
binaries installed in that directory can be invoked using the full
path or adding the directory '/snaps/bin' to the PATH environment
variable.

```
echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
```

## Useful references:

* [Getting started](https://snapcraft.io/docs/getting-started)
* [Snap confinement](https://snapcraft.io/docs/snap-confinement)
* [What’s in a snap?](https://ubuntu.com/blog/whats-in-a-snap)
