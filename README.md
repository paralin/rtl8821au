# Realtek Wireless Driver for Linux

## Alternative Repository

[This repository](https://github.com/diederikdehaas/rtl8812AU) seems to contain approximately the same codebase with several different available versions. I would recommend using it as it's more actively maintained.

## Supported chipsets
* RTL8192C
* RTL8192D
* RTL8723A
* RTL8188E
* RTL8812A (AC1200)
* RTL8821A (AC1200)
* RTL8192E
* RTL8723B

## How to (general)

1. Select your chipset and platform in `Makefile`. For example, change
```
...
CONFIG_RTL8821A = n
...
```
to
```
...
CONFIG_RTL8821A = y
...
```
and
```
CONFIG_PLATFORM_I386_PC = n
```
to
```
CONFIG_PLATFORM_I386_PC = y
```
2. `make`
3. If you have previously installed a wireless driver for your chipset, `sudo modprobe -r [your_chipset_name]` where `[your_chipset_name]` is `8821au` for example.
4. `sudo make install`
5. `sudo modprobe [your_chipset_name]`

## Release notes

```
v4.3.14_13455.20150212_BTCOEX20150128-51
Realtek release:
1. This driver can support 8811AU and 8821AU
2. Support BT coexist
3. Support Adaptivity
4. Support efuse and mac address can read from file
5. Support Sniffer feature
6. Support Linux kernel 3.16.0
7. Fix some 802.11 logo issue
8. Fix WPS issue
```


