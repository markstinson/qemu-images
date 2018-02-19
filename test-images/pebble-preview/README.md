# Pebble Preview

Link: https://drive.google.com/open?id=11J0LY-JsYUg7Blieu7afX-y4XVeM43ak

Extract `pebble_qemu_preview.7z` and run in QEMU with: `qemu-system-x86_64 -machine accel=kvm:tcg -rtc base=localtime -vga std -m 256 -usb -hda pebble_qemu_preview.vdi`
