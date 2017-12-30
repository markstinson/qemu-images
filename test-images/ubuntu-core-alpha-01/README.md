# Ubuntu Core

## Download
Link: https://drive.google.com/open?id=1IXh6dh2V3NxKLzeEIqqhWyVeMWe6uv6M

Extract `ubuntu-core-alpha-01.7z` and run in QEMU with: `qemu-system-x86_64 -machine accel=kvm:tcg -m 1024 -drive if=virtio,file=ubuntu-core-alpha-01.img,format=qcow2 -netdev user,id=user0,hostfwd=tcp::18000-:80,hostfwd=tcp::12222-:22 -device virtio-net-pci,netdev=user0`

Ubuntu Core
-----------
Contributed by Mark Shuttleworth and Alexander Sack

Ubuntu Core is a new rendition of Ubuntu for cloud container hosts. It's a tiny
image of 110 MB that is completely different to any Ubuntu you've experienced
before. In a huge break with 20 years of tradition, Ubuntu Core doesn't use DEB
packages or apt-get. Instead, it gives you transactional updates of both the
system and applications, using the new "snappy" package system based on Ubuntu
Phone's approach. The snappy approach allows for perfect updates and roll-backs
of Ubuntu and apps, independently. It also uses kernel confinement to isolate
applications from each other, so apps can be more secure by design.

You can ssh into the guest with: ssh -p 12222 ubuntu@localhost

For this alpha image there is a standard account with username "ubuntu" and
password "ubuntu".

The first thing you'll notice is that everything looks just like standard
Ubuntu on the cloud. The second thing you'll notice is that apt-get tells you
to check out "snappy --help" :)

Ubuntu Core is designed as a super reliable, super small, super secure host for
containers on the cloud. It's also designed to make it much easier for
developers to own their own packages, the snappy system is the world's simplest
packaging system (you basically zip up your app with a single tiny metadata
file). It's packaging for the github era, designed to make it as easy to share
your build of your software as it is to push your code to github.

For more information, check out https://ubuntu.com/snappy for a full
walk-through of the snappy system for installation and updates of packages, the
demo packages for docker and hello-world give you an idea of how snappy this is
to use.

IRC discussion of the snappy system that powers Ubuntu Core is on Freenode in
#snappy. Also check out https://lists.ubuntu.com/mailman/listinfo/snappy-app-devel
for building snappy apps, and https://lists.ubuntu.com/mailman/listinfo/snappy-devel
for participating in snappy's design and implementation.

Source code: http://qemu-advent-calendar.org/download/ubuntu-core-alpha-src.tar.xz
