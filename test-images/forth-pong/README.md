# Forth Pong

Link: https://drive.google.com/open?id=14paYDcSvqac5X-rlCMKmrXqRwMUOf4vV

Extract `ofpong.7z` and run in QEMU with: `qemu-system-ppc64 -M pseries-2.1 -boot order=d,strict=on -cdrom ofpong.iso`

Open Firmware Pong
----------------------------------
Disk image prepared by Thomas Huth

Play the game of Pong at the Open Firmware prompt! The game is completely
written in Forth so it can run directly with the built-in Forth interpreter
that is used in the firmware of PowerPC based server machines.

Use 's' and 'x' to control the left paddle.
Use 'k' and 'm' to control the right paddle.
Use 'q' to start a new game, and 'ESC' to quit the game.

Source code is included in the CD-ROM image:
  - mount -o loop,ro ofpong.iso /mnt
  - cat /mnt/ofpong.fs

More information:
- Original version of the game:
  http://web.archive.org/web/20080726180427/http://members.aol.com/plforth/ofpong/20020313/ofpong.txt
- Open Firmware: https://en.wikipedia.org/wiki/Open_Firmware
- Forth: https://en.wikipedia.org/wiki/Forth_%28programming_language%29
- Pong: https://en.wikipedia.org/wiki/Pong
