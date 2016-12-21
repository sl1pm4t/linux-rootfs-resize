linux-rootfs-resize
===================

Supported Linux distributions:
CentOS 6, CentOS 7, Debian 6, Debian 7, Debian 8.

This tool creates new initrd (initramfs) image with ability to resize root filesystem 
over available space. Typically you need this when you provision your virtual machine on 
a cloud provider for the first time (your image becomes flavor aware)

For now, filesystem resize is limited to ext2, ext3 and ext4 (resize2fs) including LVM volumes.

This code was successfuly tested on: CentOS 6.5, Debian 6 and Debian 7.2

DEPENDENCIES:

    cloud-utils (https://launchpad.net/cloud-utils)
    parted (CentOS)

INSTALL: 

    Install git, clone this project on your machine, run 'install'. 

On CentOS:

    cd /opt
    yum install epel-release
    yum install git parted cloud-utils
    git clone https://github.com/spetr/linux-rootfs-resize.git
    cd linux-rootfs-resize
    ./install

On Debian:

    cd /opt
    apt-get install git parted cloud-utils
    git clone https://github.com/spetr/linux-rootfs-resize.git
    cd linux-rootfs-resize
    ./install


Tool is designed in modular fashion, so support for other distributions can be added without much work (I hope).

