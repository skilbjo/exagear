# exagear

## Why

I'd like to run Mesos but Mesos only compiles on x86 machines.

Exagear is a virtual machine that translates x86 instructions to an
ARM instruction set. However exagear is meant for a debian system,
not arch linux.

## Install

Make some aliases

    sudo -s
    echo alias arch="echo 'armv7l'" >> /root/.bashrc
    alias realpath="/usr/bin/realpath" >> /root/.bashrc
    alias bash="/usr/bin/bash" >> /root/.bashrc
    alias awk="/usr/bin/awk" >> /root/.bashrc

Clone this repo on the target ARM device.

    bin/pack-deb src/eltechs-deb/arch-linux/
    mv fixed.deb exagear.deb
    bin/pack-deb src/ubuntu-deb/arch-linux/
    mv fixed.deb ubuntu.deb
    sudo bin/install-on-archlinux

## Use

What is available: `exagear ls`

Turn exagear on: `exagear`

Turn exagear off: `exagear` ;; TODO is this the correct command?

## Debug

    System memory configuration is determined as 2g/2g
    ARCH=armv7l
    ls: cannot access '/opt/exagear/images/': No such file or directory
    HOST OS: arch
    HOST OS VERSION: default
    EXAGEAR package: exagear-mem2g_*-1_armhf.deb
    EXAGEAR guest image package: 'exagear-guest-ubuntu-1404lts_*_all.deb'
    Installing prerequisites...
    Installing the binary translator...
    Installing the guest image...
    Installing the primary key...
    actool: Found no primary key file.
