# qemu-images
A collection of disk images that can be used by the QEMU emulator. If you are installing an OS in QEMU but don't want to go through the whole process of downloading an ISO, preparing a disk image, waiting for the install to complete, etc, you can use one of my prepared images that I have created. In most cases, the images are vanilla installations, meaning they are un-modified from the original installation. If you want to just experiment with QEMU and see what it can do, check out the test-images folder!

## What is QEMU?
QEMU (short for Quick Emulator) is an processor emulator. By using QEMU, you can run operating systems for different CPU architectures regardless of your host CPU's architecture. You can run IA-32 (x86), x86-64, ARM, PowerPC, and lots more! QEMU can be installed on the host computer or ran from a USB flash drive. QEMU makes for a great alternative to VirtualBox and VMware, especially since these two programs are restricted to running guest operating systems for the x86 architecture.

## How do I obtain QEMU?
- If you use Linux:
  - `apt-get install qemu`
- If you use Windows:
  - Go to: https://qemu.weilnetz.de/ and go to either the w32 or w64 directory and download one of the .exe files. In general, it's OK to download the most recent installer
  - If you installed it on your PC (not a USB) and you want to access it anywhere from the terminal, add it to your PATH environement variable. This does not happen by default.
  - If you feel really unconfortable with the command line on Windows, then you can run the setupqemuk70.exe installer. Note that this holds a very old version of QEMU that may not work with all the examples in this repository, so you might as well install a newer version and get used to the command line

## How do I run the examples in this repository?
- In each directory exists instructions to run their respective disk images.

## I went to a directory but there was no disk image!
- There will be a link in the directory's README to download the file seperately.

## Why are all of the disk images in .7z format?
- In general, disk images can be fairly large in size. In most cases, .7z format has better compression than .zip and other compression formats

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
