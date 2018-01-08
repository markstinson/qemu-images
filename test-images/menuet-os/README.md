# MenuetOS

Link: https://drive.google.com/open?id=1enNW3_yCBaUc01RIWlVHqYQlrvJ9fM70

Extract `M32-086.7z` and run in QEMU with: `qemu-system-x86_64 -M accel=kvm:tcg -soundhw ac97 -m 512 -drive file="M32-086.IMG",format=raw,if=floppy`

MenuetOS (32-bit)
-----------------

When answering the questions during the boot process, use "1" for PS/2
mouse and "5" for 512 MB RAM.

More information from the MenuetOS website:

MenuetOS is a pre-emptive, real-time and multiprocessor Operating System in
development for the PC written entirely in 32/64 bit assembly language.
Menuet64 is released under License and Menuet32 under GPL. Menuet supports
32/64 bit x86 assembly programming for smaller, faster and less resource
hungry applications.

Menuet isn't based on other operating system nor has it roots within UNIX or
the POSIX standards. The design goal has been to remove the extra layers
between different parts of an OS, which normally complicate programming
and create bugs.


See the website http://menuetos.net/ for more information, and for Menuet64
downloads, which is an improved, 64-bit version of MenuetOS (and is licensed
differently).

