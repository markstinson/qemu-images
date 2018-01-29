# Damn Vulnerable Linux v1.0

Link: https://drive.google.com/open?id=1pajZ55bz1sL-MYQO8CB4aUeyroeNImD-

Extract `dvl-1.0.7z` and run in QEMU with: `qemu-system-i386 -hda dvl-1.0.qcow2 -m 512`

## Install Info
- 1 GiB in total virtual size

The install is so fresh that users have not even been setup.

Here are the steps to take when you first run the system:
1. It will prompt you for a new password for `root`. Enter a new password.
2. It will then prompt you for a new password for user `dsl`. Enter a new password.
3. It will then prompt you with `box login: `. Enter `dsl` then enter the password you gave `dsl` earlier.
4. In a few more seconds it will boot up with a graphical desktop.

Damn Vulnerable Linux (DVL) is everything a good Linux distribution isn't. Its developers have spent hours stuffing it with broken, ill-configured, outdated, and exploitable software that makes it vulnerable to attacks.

It's based on the popular mini-Linux distribution Damn Small Linux (DSL), not only for its minimal size, but also for the fact that DSL uses a 2.4 kernel, which makes it easier to offer vulnerable elements that might not work under the 2.6 kernel.

It contains older, easily breakable versions of Apache, MySQL, PHP, and FTP and SSH daemons, as well as several tools available to help you compile, debug, and break applications running on these services, including GCC, GDB, NASM, strace, ELF Shell, DDD, LDasm, LIDa, and more.

DVL was initiated by Thorsten Schneider of the International Institute for Training, Assessment, and Certification (IITAC) and Secure Software Engineering (S�e) in cooperation with Kryshaam from the French Reverse Engineering Team. "The main idea behind DVL," says Schneider, "was to build up a training system that I could use for my university lectures." His goal was to design a Linux system that was as vulnerable as possible, to teach topics such as reverse code engineering, buffer overflows, shellcode development, Web exploitation, and SQL injection.
