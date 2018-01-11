# KolibriOS

Link: https://drive.google.com/open?id=1IO2nn65idryYcAoTcFQ2qVCt6FUij5yd

Extract `kolibri.7z` and run in QEMU with: `qemu-system-x86_64 -machine accel=kvm:tcg -device e1000,vlan=0 -net user -usb -device intel-hda -device hda-duplex -boot d -cdrom kolibri-v2.iso`

KolibriOS
=========
[Disk image put together by Kashyap Chamarthy <kashyapc@fedoraproject.org>
 v2: Removed the HD_Load folder with Windows exe files from the iso
     since some virus scanners were reporting false positives for these]

"KolibriOS is a tiny yet incredibly powerful and fast operating system.
This power requires only a few megabyte disk space and 8MB of RAM to
run. Kolibri features a rich set of applications that include word
processor, image viewer, graphical editor, web browser and well over 30
exciting games. Full FAT12/16/32 support is implemented, as well as
read-only support for NTFS. [...]  Written entirely in Assembler/FASM."

It boots in less than 10 seconds from power-on to working GUI.

Website: http://kolibrios.org/

Sources: http://qemu-advent-calendar.org/2016/download/kolibrios-src.tar.xz

Video: "KolibriOS on eBox-3350MX (tiny x86 PC)" --
https://www.youtube.com/watch?v=XnlA4ijrTBo
