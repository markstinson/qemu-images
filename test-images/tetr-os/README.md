# TetrOS

Link: https://drive.google.com/open?id=1SZplGAHzkpVS2GFpVl3sw7HGL-Fot5Ci

Extract `tetros.7z` and run in QEMU with: `qemu-system-i386 -M accel=kvm:tcg -m 32 -drive "if=ide,file=tetros.img,format=raw"`

TetrOS
--------------------------------------
Daniel E with contributions from Noah Rosamilia & Hayden E. Davies
Disk image prepared by Stefan Hajnoczi

This is a falling blocks game with one special feature: it fits into the Master
Boot Record.  The game is only 446 bytes so it can be booted from the first
sector of a disk or USB stick without a bootloader or operating system.

In order to keep the size small the game is implemented in x86 assembly.
Several features like scores or title screens were omitted to fit into the
limited space.

The game runs in 16-bit real-mode, the environment that bootloaders start in.
The only available interfaces are the BIOS interrupts, a somewhat standard set
of utilities for reading the disk, keyboard input, etc.

Use Left and Right arrow keys to move the block, Up and Down arrow keys to
rotate.

More information:
- https://github.com/daniel-e/tetros
- https://en.wikipedia.org/wiki/Real_mode
- https://en.wikipedia.org/wiki/BIOS_interrupt_call
