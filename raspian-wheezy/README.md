# Raspberry Pi running Raspian Wheezy
Link:

Extract raspian-wheezy-disk-image-and-kernel.7z and run with: `qemu-system-arm -M versatilepb -cpu arm1176 -hda 2012-07-15-wheezy-raspbian.img -kernel kernel-qemu -m 192 -append "root=/dev/sda2"`
