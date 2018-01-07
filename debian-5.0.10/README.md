# Debian 5 Final - "Lenny"

Debian 5.0.10 "Lenny" i386 (32-bit) and amd64 (64-bit) images for QEMU. Images are 25GiB images in QCOW2 format on which a Debian Lenny 5.0.10 system has been installed. Images contain a minimum system with only the standard system utilities installed, so there is no graphical desktop environment (although you can always add one if you'd like i.e. Gnome, KDE, etc).

## Downloads
32-bit:

64-bit:

Un-compress the .7z files to retrieve the .qcow2 images

## Install Info
The other installation options are the following:
- Keyboard:       US
- Locale:         en_US
- Timezone:       Pacific
- Mirror:         N/A (Read below on how to install packages from the Debian archive mirror)
- Hostname:       debian
- Root password:  root
- User account:   user
- User password:  user

To use these images, you need to install QEMU 1.1.0 (or later) or a recent KVM version. Start QEMU or KVM with the image as argument:
- 32-bit: `qemu-system-i386 -hda debian-5.0.10-i386.qcow2`
- 64-bit: `qemu-system-x86_64 -hda debian-5.0.10-amd64.qcow2`

When ran on an amd64 host with hardware virtualization, and when the KVM module is loaded and accessible to the user, it is possible to use the -enable-kvm option to run the guest faster. By default QEMU emulates a machine with 128MiB of RAM. The -m option increases or decreases the size of the RAM. If you don't want to start QEMU in graphic mode, you can use the -curses option.

## How to add packages and software/connect to the package repository
As root, if you attempt to install any packages via `apt-get install` it will halt and prompt for the install DVD that was used for this system. Also, since this version of Debian is older, a package mirror was not selected at install time. If you would like to use the archive mirror to install packages and security updates, open your `/etc/apt/sources.list` in a text editor and replace the entire file contents with the following:

```
deb http://archive.debian.org/debian/ lenny main non-free contrib
deb-src http://archive.debian.org/debian/ lenny main non-free contrib

deb http://archive.debian.org/debian-security/ lenny/updates main non-free contrib
deb-src http://archive.debian.org/debian-security/ lenny/updates main non-free contrib
```
Since this is an "un-touched" system, I did not want to "taint" anything by making modifications after the installation.

Many thanks to Aurelien's example images: https://people.debian.org/~aurel32/qemu/ and the example README! Note that these images are not the same as Aurelien's images.
