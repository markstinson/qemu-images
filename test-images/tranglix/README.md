# Trianglix

Link: https://drive.google.com/open?id=1ULJGV4Mlmt_StdjqipDtrieo8r_zZb50

Extract `trianglix.7z` and run in QEMU with: `qemu-system-x86_64 -M accel=kvm:tcg -m 1024 -vga std -drive file=trianglix.qcow2,format=qcow2`

Trianglix with Sortix
---------------------

[Disk image prepared by Kashyap Chamarthy <kashyapc@fedoraproject.org>]

Trianglix is an orthogonal multi-user secure self-hosting Triangle
System written entirely from scratch.

Trianglix uses the paradigm that everything is a triangle, in stark
contrast to the Unix principle that everything is a file. 

Each triangle has three edges (input, output and error) and represents a
Turing-computable triangular function, expressed through well-formed
Triscript written in Runes and senary digits. Triscript is a powerful
and expressive language unlike anything ever developed before. It
doesn't belong in the classic categories of programming languages such
as imperative or functional, but is perhaps best described as angular
flow-like esoteric programming. The system is implemented as a series of
executable triangle servers wrapped around the all-powerful core Trinit
root triangle, which is built upon the kernel angular virtual machine.

NOTES
~~~~~

  - To change resolution, invoke the command `chvideomode` and press 
    enter.

  - You can type `sh` (or navigate to Development |> Shell) to get a   
    shell in the Unix compatibility environment that only crazy circular 
    people would use.

  - NB: Runes are the optimal character system for triangle-character
    representation. New users will experience a temporary Latin
    character compatibility mode while they get accustomed to runes.
    Should you need additional learning time, select |Administration>
    |Disable Runes>.  (https://en.wikipedia.org/wiki/Runes)

References
~~~~~~~~~~

- Trianglix: https://sortix.org/trianglix/
- Sortix: https://sortix.org/

* * *
