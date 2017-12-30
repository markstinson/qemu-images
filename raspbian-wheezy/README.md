# Raspberry Pi running Raspbian Wheezy
Link: https://drive.google.com/open?id=1nkzbois7QuI28c-9hKMW3vO-Wd7DFGbS

Extract raspbian-wheezy-disk-image-and-kernel.7z and run with: `qemu-system-arm -M versatilepb -cpu arm1176 -hda 2012-07-15-wheezy-raspbian.img -kernel kernel-qemu -m 192 -append "root=/dev/sda2"`
