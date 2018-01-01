# linux-custom
These are scripts for Archlinux to automake kernel. Easy to use, but be careful.

Follow the steps to build your kernel:
1) put these scripts in one directory, say "test"
2) cd to the test, and modified the PKGBUILD, and change the source to the git address you like, e.g., git+https://github.com/OpenChannelSSD/linux.git#branch=pblk.cnex
3) set pkgver to your own version, e.g. pkgver=4.14.0.rc2
4) makepkg, and after a while, you will see pkg.tar.xz files and some new directories
5) sudo pacman -U linux-xxx.pkg.tar.xz, install your kernel
6) sudo pacman -U linux-headers-xxx.pkg.tar.xz, install your kernel headers
7) sudo vim /boot/grub/grub.cfg, add your new boot option to this file. You can add it before the old options in order to make the new option default.
8) sudo reboot, and you will see your new boot option.
