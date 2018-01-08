# Tower of Hanoi

Link: https://drive.google.com/open?id=1_J1cqg6Yd-JA2h0j-ws2xmfJQZ733its

Extract `hanoi.7z` and run in QEMU with: `qemu-system-ppc64 --boot order=d,strict=on -g 800x600x8 --cdrom hanoi.iso`

The Tower of Hanoi by Amit Singh
----------------------------------
Disk image prepared by Thomas Huth

This little Forth program plays the Tower of Hanoi game in Open Firmware.

The OpenFirmware standard is used by PowerPC and SPARC machines and includes
a Forth environment for diagnostics, boot scripts, and even device drivers
similar to x86 PCI option ROMs.

Forth is a stack-based language that appeared in the 1970s and has been used in
firmware and embedded systems.

Source is included in the CD-ROM image:
  # mount -o loop,ro hanoi.iso /mnt
  # cat /mnt/hanoi.fs

Original version has been taken from:
 http://www.kernelthread.com/projects/hanoi/src/hanoimania/hanoi-gfx.macprom

More information:
- Open Firmware: https://en.wikipedia.org/wiki/Open_Firmware
- Forth: https://en.wikipedia.org/wiki/Forth_%28programming_language%29
- Tower of Hanoi: https://en.wikipedia.org/wiki/Tower_of_Hanoi

