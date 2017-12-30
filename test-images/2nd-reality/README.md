# 2nd Reality

Link: https://drive.google.com/open?id=1fcF-Glb_-zW2JaLixVJzs5f3bkUR36b-

Extract 2nd-reality.7z for the disk image. Run in QEMU with the following: `qemu-system-i386 -machine accel=tcg -vga std,retrace=precise -soundhw gus 2nd-reality.qcow2`

Info
-----------
Demo by Future Crew, disk image prepared by Paolo Bonzini

Second Reality is a groundbreaking demo from the 1990s PC demo scene.  It
features 2D and 3D rendering techniques synchronized with a soundtrack.

Be warned, this demo requires a fast 33 MHz 486 machine!

Somewhat embarrassingly, in 2014 it still pushes the boundaries of QEMUs
graphics emulation :-).

Wikipedia: https://en.wikipedia.org/wiki/Second_Reality

Source code: https://github.com/mtuomi/SecondReality
