# MPRO DRM

A simple DRM driver for VoCore MPRO screen.

# Usage

This repository provides multiple branches corresponding to different kernel versions. You can select the corresponding branch based on the kernel version you are using, and then execute the following command to install the module into the system.

For linux 6.12.

```
git clone https://github.com/Vonger/mpro_drm
cd mpro_drm
make
sudo make install
```

# Usage for Raspberry Pi OS

> Note: At the time of writing this document, the latest Raspberry Pi OS uses 6.6 kernel.

We can install the MPRO DRM driver into the Raspberry Pi OS through the following command line operations.

```
git clone https://github.com/ieiao/mpro_drm.git
cd mpro_drm
# this part you can choose your linux kernel version.
git checkout -t origin/6.6.y-dma
make
sudo make install
```

After executing the above command, you can test whether the driver can be loaded properly by restarting or executing the `sudo modprobe mpro` command.

![](imgs/rpios.webp)
