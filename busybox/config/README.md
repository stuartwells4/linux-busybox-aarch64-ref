Busybox Reference
====

The kernel files will be large, once you install into location, reduce the symbols:

find . -name *.ko -exec strip --strip-unneeded {} +

To create an initrd file using cpio, use the following command:

find . -print0 | cpio --null -ov --format=newc | gzip -9 > ../initramfs.cpio.gz

