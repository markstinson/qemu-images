# Bootable Pi

Link: https://drive.google.com/open?id=1OFykLvG8uTZwk36aon9KC7RT_3VeU491

Extract pi.7z for the disk image. Run in QEMU with the following: `qemu-system-i386 pi.vfd`

Digits of Pi
------------
Prepared by Paolo Bonzini, based on pi_10.com. This is a tiny boot sector that calculates the digits of Pi.

View assembly source: mount pi.vfd /mnt

How does this tiny boot sector calculate digits of pi? Disassemble with `objdump -D -b binary -m i8086 pi.vfd` or mount the disk image's FAT file system to view the source.
