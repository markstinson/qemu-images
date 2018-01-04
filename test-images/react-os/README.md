# ReactOS

Link: https://drive.google.com/open?id=1irgRPIgf7OOrWy6xD7XQEfRoHLQrRfZl

Extract `ReactOS-0.4.3-live.7z` and run in QEMU with: `qemu-system-x86_64 -M accel=kvm:tcg -m 512 -net nic,model=rtl8139 -net user -vga std -soundhw ac97 -usb -device usb-tablet -cdrom ReactOS-0.4.3-live.iso`

ReactOS
-------

Information about ReactOS from the FAQ at http://reactos.org/joining/faqs:
ReactOS is a free and open source operating system written from scratch.
Its design is based on Windows in the same way Linux is based on Unix, however
ReactOS is _not_ linux. ReactOS looks and feels like Windows, is able to your
run Windows software and your Windows drivers, and is familiar for Windows
users.

Have a look at https://www.reactos.org/wiki/Tests_for_0.4.3 for a list of
Windows applications that can already be used with ReactOS.
