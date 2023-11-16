# manifest_genio_compute

This repo contains manifests used for building Genio Compute Distro, which is
a new distro specifically for Genio compute board.

## How to use

To build the distro, please follow the regular Yocto build procedure described below:

    $ mkdir genio-compute; cd genio-compute
    $ repo init -u https://gitlab.com/mediatek/aiot/pilot/compute/manifest_genio_compute.git -b dev/kirkstone -m default.xml
    $ repo sync -j12
    $ TEMPLATECONF=$PWD/src/meta-mediatek-compute/conf source src/poky/oe-init-build-env
    $ MACHINE=genio-1200-evk bitbake genio-compute-image

