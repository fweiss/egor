- /boot/dtb/rockchip/rk3588s-orangepi-5-pro.dtb

``dtc -I dtb -O dts input.dtb | less``

```
        i2s@fddc0000 {
                compatible = "rockchip,rk3588-i2s-tdm";
                reg = <0x00 0xfddc0000 0x00 0x1000>;
                interrupts = <0x00 0xb8 0x04>;
                clocks = <0x02 0x1fb 0x02 0x1fb 0x02 0x1f0>;
                clock-names = "mclk_tx\0mclk_rx\0hclk";
                assigned-clocks = <0x02 0x1f9>;
                assigned-clock-parents = <0x02 0x05>;
                dmas = <0xee 0x00>;
                dma-names = "tx";
                power-domains = <0x06 0x19>;
                resets = <0x02 0x38d>;
                reset-names = "tx-m";
                rockchip,playback-only;
                #sound-dai-cells = <0x00>;
                status = "disabled";
                phandle = <0x24a>;
        };

also
- i2s@fddf0000
- i2s@fddfc000
- i2s@fe470000
- several more but not rk3588
```

## enable i2s
Add ``dtparam=i2s=on`` to /boot/armbian...txt``

## disable leds
orangepi-5-pro-disable-leds.dtbo

> the overlays didn't work

edit ``/etc/armbian-leds.conf``
``s/heartbeat/none/g``

argh!

[this solution finally worked!](https://forum.radxa.com/t/how-to-turn-off-blue-led-or-green-led-under-armbian-system/15264/2)

```
STOP the ‘armbian-led-state.service’ by running the command
sudo systemctl stop armbian-led-state.service
EDIT the config file ‘/etc/armbian-leds.conf’
sudo vi /etc/armbian-leds.conf
Change the value for the entity ‘trigger’ of section ‘[/sys/class/leds/blue:heartbeat]’ to ‘none’ so it looks like this:
[/sys/class/leds/blue:heartbeat]
trigger=none
brightness=0
START the ‘armbian-led-state.service’ again by running the command
sudo systemctl start armbian-led-state.service
Voila, done!
```
