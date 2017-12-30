# Multiboot Invaders

Link: https://drive.google.com/open?id=1mMWjGVtw2zf_g9a5Z53OAEA9l10n469B

Extract invaders.7z for the disk image. Run in QEMU with the following: `qemu-system-x86_64 -machine accel=kvm:tcg -kernel invaders.exec`

From http://www.qemu-advent-calendar.org/2014/: "The Multiboot boot sequence is supported by the GRUB bootloaders and QEMU as a way to standardize common mechanisms like kernel command-lines, modules/initrd, x86 protected mode, and graphics mode at startup. This little spaceship game is implemented as a Multiboot-compliant binary so it can be loaded directly by QEMU."

Image prepared by Fam Zheng and Fabian Greffrath, game written by Eric Thiele

Fight the aliens!

Use left & right to move, space to shoot.

Website: http://www.erikyyy.de/invaders/

Source code: http://qemu-advent-calendar.org/download/invaders-1.0.0.tar.gz
