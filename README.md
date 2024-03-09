# nanobyte_os
This repository contains the code from the by students of National Institute of Technology, Srinagar 2020-24 batch Group 4.
```
Group Members:
1.Parath Safaya
2.Hemanshu Sharma
3.Rishav Hodoker
4.Rohit Katal
5.Nitin Sharma
```

## Building

First, install the following dependencies:

```sh
# Ubuntu, Debian:
sudo apt install build-essential bison flex libgmp3-dev libmpc-dev libmpfr-dev texinfo wget \
                   nasm mtools python3 python3-pip python3-parted scons dosfstools libguestfs-tools qemu-system-x86

sudo pip3 install sh pyelftools

# Fedora:
sudo dnf install gcc gcc-c++ make bison flex gmp-devel libmpc-devel mpfr-devel texinfo wget \
                   nasm mtools python3 python3-pip python3-pyparted python3-scons dosfstools guestfs-tools qemu-system-x86

sudo pip3 install sh pyelftools

# Arch & Arch-based:
paru -S gcc make bison flex libgmp-static libmpc mpfr texinfo nasm mtools qemu-system-x86 python3 python3-scons

sudo pip3 install sh pyelftools
```
NOTE: to install all the required packages on Arch, you need an [AUR helper](https://wiki.archlinux.org/title/AUR_helpers).

After that, run `scons toolchain`, this should download and build the required tools (binutils and GCC). If you encounter errors during this step, you might have to modify `build_scripts/config.mk` and try a different version of **binutils** and **gcc**. Using the same version as the one bundled with your distribution is your best bet.

Finally, you should be able to run `scons`. Use `scons run` to test your OS using qemu.

