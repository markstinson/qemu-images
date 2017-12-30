# Early Slackware

Link: https://drive.google.com/open?id=1dP_TM5d6YecLk_Oy-bHCdnKMFBUb53fA

Extract slackware.7z for the disk image. Run in QEMU with the following: `qemu-system-x86_64 -m 16M -drive if=ide,format=qcow2,file="slackware.qcow2" -netdev user,id=slirp -device ne2k_isa,netdev=slirp`

Below is the original documentation from Patrick J. Volkerding.

Ready for a time travel?
------------------------

From: Patrick J. Volkerding (volkerdi@mhd1.moorhead.msus.edu)
 Subject: [ANNOUNCE] Slackware Linux 1.01 
 Newsgroups: comp.os.linux.announce
 Date: 1993-08-04 08:33:56 PST 


The Slackware Linux distribution (v. 1.01) is now available for 
anonymous FTP. This is a complete installation system designed for
386/486 systems with a 3.5" boot floppy. 486 optimizations are now 
used for most of the included software.

[ ... ]


What is it?
-----------

Slackware it's the oldest linux distribution which is still active
today.  Thats why you can find old releases on the internet without
too much trouble.  So I went ahead, grabbed the oldest release I could
find, installed & configured it for you to play with.


Quickstart
----------

Use the Run script to boot.  Login as root (no password).


Hints and background info
-------------------------

Surprisingly booting to the login prompt works just fine with the
default qemu configuration.  Sometimes it helps if there is backward
compatibility in the hardware, so one can drive pci ide and pci vga
without knowing anything about pci ...

While being at it: There was no pci in 1993.  Therefore a pci nic
isn't going to fly.  Use ne2k_isa.

There was no dhcp in 1993.  The disk image has a static network
configuration.  It assumes qemu default slirp configuration, so use
that if you want a working network without fiddeling with ifconfig
(which doesn't understand 10.0.2.0/24 syntax yet) and route.

The number of available keymaps is pretty limited, see
/usr/lib/keytables.  Default is us.  If that troubles you use the
getty at the serial line to login.

The system runs without any problems with 16 MB of memory.
Kernel version is 0.99pl12, release notes: /usr/src/linux/README.
gcc version is 2.4.5.
Boot loader is lilo (no need for a boot floppy, yay!).
There is no /sbin.  System binaries are in /etc.
There is no ssh.  You can use rsh for remote logins.
No power management.  No SMP.  No systemd.

Alot of funky network services are active by default (and I left them
on to not spoil the fun).  So better don't hook that machine to the
public internet, it might be owned within seconds.  On the other hand
todays hackers probably concentrate on other kinds of attacks, so it
might not be that dangerous after all ...

The web browser is called 'telnet'.  Support for http and html is very
limited.  Enter 'telnet <server> 80' at the shell prompt, then go type
the http request.  Check RfC 2616 for details.  Due to lack of support
for images, css and javascript the browser is not vulnerable to cross
site scripting, web bugs and other modern attacks.

enjoy!
