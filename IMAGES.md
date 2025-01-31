orange pi 5 pro images

http://www.orangepi.org/html/hardWare/computerAndMicrocontrollers/service-and-support/Orange-Pi-5-Pro.html

## Ubuntu
- Orangepi5pro_1.0.6_ubuntu_jammy_server_linux6.1.43
- didn't have the 0.9.7 driver

## Debian
- Orangepi5pro_1.0.6_debian_bullseye_server_linux6.1.43
- python 2.7
- RKNPU driver: v0.9.6
- has orangepi-congif - can disable leds


## Joshua Riek
- did have the 0.9.7 driver
- no python3
- no cmake, etc
- no orangepi-config

## Armbian
[support](https://www.armbian.com/soc/rk3588/)
> root/1234
> You are using an automated build meant only for developers
>  don't use this image for production
- kernel: 6.1.84-vendor-rk35xx
- python3: 3.11.2
- no gcc, cmake, make, etc
- RKNPU driver: v0.9.8
- GNU Wget 1.21.3 built on linux-gnu
- no git
- no orangepi-config - armbian-config instead
- ssh orangepi@orangepi5pro

## Links and references
[open source rknpu driver](https://blog.tomeuvizoso.net/2024/06/rockchip-npu-update-4-kernel-driver-for.html)

[pelochus custom kernel](https://github.com/Pelochus/armbian-build-rknpu-updates)
