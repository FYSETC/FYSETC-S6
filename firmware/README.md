# Firmware

The Marlin default configurations are below:

```
#define BAUDRATE 115200
#define MOTHERBOARD BOARD_FYSETC_S6_V2_0
#define SDSUPPORT
#define TOUCH_UI_FTDI_EVE
```

You need to change configurations for you own machine. 

# Pre-builds

If you use `Marlin-0x8000.bin` then you need the bootloader `Bootloader-FYSETC_S6.hex`. And if you use `Marlin-0x10000.bin`, you need bootloader named `Bootloader-FYSETC_S6_10000.hex`. You can get the bootloader [here](https://github.com/FYSETC/FYSETC-S6/tree/main/bootloader).

