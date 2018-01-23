# 64-bit ARM

Link: https://drive.google.com/open?id=1ePeHHdTDE-vV7x2ruv3vGa3XPVSJKxm1

Extract `arm64.7z` and run in QEMU with `qemu-system-aarch64 -m 1024 -cpu cortex-a57 -machine virt -nographic -kernel Image -append 'root=/dev/vda2 rw rootwait mem=1024M console=ttyAMA0,38400n8'  -drive if=none,id=image,file=armv8.qcow2 -netdev user,id=user0 -device virtio-net-device,netdev=user0  -device virtio-blk-device,drive=image -redir tcp:5555::22`

64-Bit ARM support in QEMU
-----

QEMU is the first open source emulator to support 64-Bit ARM architecture.
This demo image requires qemu 2.1 or newer. 

Apart from the some unfamiliar items in /proc/cpuinfo or unusual
prints from "dmesg" command, this image offers almost no surprises. It
looks and feels just like any other bleeding edge Linux system -
3.18 based kernel with virtio guest drivers boots in a moment. 

for convenience you get a root prompt on serial without password. or you can
log in from ssh (listening on port 5555).

Once you get bored with the minimal system,  just run "tetris-bsd" command to
train vi navigation keys :)
