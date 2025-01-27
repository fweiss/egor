# Setup
Outline of the Orange Pi 5 Pro User Manual

## Boot media configurations
User Manual sections shown in parenthesis.
- TF card (2.3, 2.4)
- eMMC (2.5)
- TF card+NVMe SSD (2.6)
- SPIFlash+NVMe SSD (2.7)
- SPIFlash+SATA SSD (2.8)
- SPIFlash+USB thumb drive (2.9)

> I think the boot order is TF Card, then EMMC (or SPI). 
> looks like there's no direct boot off of NVME.
> The TF Card can be flashed with ``rkspi_loader.img``
> which prevents the OS image on the TF Card for loading.

> It looks like flashing the image onto NVME does partiion.
> There's a 256 MB partion for /boot, the rest is root /.

> Flashing directly to NVME SSD is possible over the special
> USB port, a driver on Windows, and a ImageLoader on Windows.
> Need to hold the MASKROM button to enter this mode.
> Not clear if flashing the NVME SSD this way overwrites the
> root file system.

> Ultimately, use an OTA framework like Mender, SWUpdate, BalenaEtcher, or RAUC 
> for managing updates automatically.

> Safest bet - at least for prototyping - is to just use TF Card for OS updates and mount the
> NVME SSD for software models.

## Host systems
- Windows
- Ubuntu

## Tools
- belenaEtcher
- RKDevTool
- Win32DiskImager
- dd command

## Images
- Linux
- OpenWRT
- Android
- Orange Pi OS (Droid)

## Actions
- clear APIFlash
- start the dev bvoard
- debugging via serial port
- supplying power
- Xfce
- Linux login
- disable desktop

## Other tasks
- onboard LED
- network connection
- ssh
- adb
- uploading files
- hdmi
- bluetooth
- USB
- Audio
- SSD

## developer
- temperature sensor
- 40 pin interface
- wiringOP
- 40 pin peripherals
- wiringOP PWM
- wiringOP Python
- hardwre watchdog

## more
- NPU [3.37-39]
- etc

## NPU
- RKLLM toolchain [3.39.1.1]
Pages 413-480

## Turn off flashing blue and green LEDs
- ``sudo orangepi-config``
- navigate to System > Hardware
- tick ``opi5pro-disable-leds``
- select Save, Back, Reboot

## Links and references
[Joshua Riek Ubuntu Rockchip](https://github.com/Joshua-Riek/ubuntu-rockchip)


