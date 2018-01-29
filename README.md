# qemu-images
A collection of disk images that can be used by the QEMU emulator. If you are installing an OS in QEMU but don't want to go through the whole process of downloading an ISO, preparing a disk image, waiting for the install to complete, etc, you can use one of my prepared images that I have created. In most cases, the images are vanilla installations, meaning they are un-modified from the original installation. If you want to just experiment with QEMU and see what it can do, check out the [test-images](https://github.com/palmercluff/qemu-images/tree/master/test-images) folder!

Some of these disk images can even be ran in other emulators, such as the [Limbo PC Emulator App for Android](http://limboemulator.weebly.com/) (which is actually a derivation of the original QEMU emulator). Yes, you can run other operating systems on Android with this! Known images to work in Limbo PC Emulator are: FreeDOS, DSL, and other small linux distros.

## What is QEMU?
QEMU (short for Quick Emulator) is an processor emulator. By using QEMU, you can run operating systems for different CPU architectures regardless of your host CPU's architecture. You can run IA-32 (x86), x86-64, ARM, PowerPC, and lots more! QEMU can be installed on the host computer or can be ran from a USB flash drive. QEMU makes for a great alternative to VirtualBox and VMware, especially since these two programs are restricted to running guest operating systems for the x86 architecture.

## How do I obtain QEMU?
- If you use Linux:
  - `apt-get install qemu`
- If you use Windows:
  - Go to: https://qemu.weilnetz.de/ and go to either the w32 or w64 directory and download one of the .exe files. In general, it's OK to download the most recent installer
  - If you installed it on your PC (not a USB) and you want to access it anywhere from the terminal, add it to your PATH environement variable. This does not happen by default.
  - If you feel really unconfortable with the command line on Windows, then you can run the setupqemuk70.exe installer. It can be downloaded [here](https://drive.google.com/open?id=1e0A9OmJoRkopfYvsW4dGaUzCx0H_kIwQ). Note that this holds a very old version of QEMU that may not work with all the examples in this repository, so you might as well install a newer version and get used to the command line
- If you use Mac OS X:
  - QEMU can be installed from Homebrew `brew install qemu`

## How do I run the examples in this repository?
- In each directory exists instructions to run their respective disk images.

## I went to a directory but there was no disk image!
- There is a link in the directory's README to download the file(s) seperately.

## Why are all of the disk images in .7z format?
- In general, disk images can be fairly large in size. In most cases, .7z format has better compression than .zip and other compression formats. You will need to use a tool such as 7-zip to extract the disk image.

## How can I make my own disk image? Can I create one from scratch?

- Yes, here is a brief tutorial:

- First, you need some sort of ISO. We will use FreeDOS as an example
  - Download the FreeDOS ISO file at: http://www.freedos.org/download/download/FD12CD.iso
  - Move it to a directory other than your "Downloads" folder if you'd like
  
- Create a hard disk image with `qemu-img create`
  - For a raw image format: `qemu-img create myImage.img 1G` or with qcow2 image format: `qemu-img create -f qcow2 myImage.qcow2 1G` where `myImage` is the name for your disk image file and `1G` is the size of the file. Note that by using the qcow2 image format, you might be able to save some space on your hard drive or USB stick

- Boot QEMU with the ISO mounted and disk image attached
  - `qemu-system-i386 -hda myImage.img -cdrom FD12CD.iso -boot d -m 256`
    - `-boot d` - Boot the first virtual CD-ROM drive
    - `-m 256`  - Give the machine 256 MB of RAM
    
- From here just follow the install instructions for the OS
  - Link: http://wiki.freedos.org/install/

- After the installation is done, the system can be booted with:
  - `qemu-system-i386 -hda myImage.img -m 256`

## Can I run these images in VirtualBox instead?
- Yes, but there are a couple things you need to do first:
  1. You need to make sure the original image is x86 or x64 compadable, i.e. the image is for the i386 or amd64 architecture, and that the image can originally be ran with the `qemu-system-i386` or `qemu-system-x86_64` command(s)
  2. You need to convert the .img or .qcow2 into a .vdi
     - From raw to vdi: `qemu-img convert myImage.img -O vdi vdisk.vdi`
     - From QCOW2 to vdi: `qemu-img convert -f qcow2 myImage.qcow2 -O vdi vdisk.vdi`

## How can I get disk information (i.e. Type of disk image, virtual size, etc)?
- `qemu-img info <disk-image-file>`
