# tester
test
title Ubuntu 12.10
find --set-root /ubuntu-12.10-desktop-i386.iso
map /ubuntu-12.10-desktop-i386.iso (hd32) || map --mem /ubuntu-12.10-desktop-i386.iso (0xff)
map --hook
root (hd32)
kernel /casper/vmlinuz boot=casper iso-scan/filename=/ubuntu-12.10-desktop-i386.iso quiet splash --
initrd /casper/initrd.lz
