# OS

## SAMFi-OS_OrangePi_zero

Before you config the [SAMF-OS_OrangePi_zero](https://github.com/FYSETC/FYSETC-SAMFi-OS). You need an TF card with at least 8G capacity.

### Step 1

Download and flash the OS image with `balenaEtcher` software to your TF card. Insert your flashed TF card to OrangePi-zero and connect Ethernet cable then power on. Find the ip address of OrangePi-zero on your router, host name is `orangepizero`.

![](OrangePi-zero\OrangePi_zero.jpg)

### Step 2

You can find the firmware `klipper.bin` in `OrangePi-zero` folder after you download the github repository. It is also stay in the OS path `firmwares\s6.bin` after you login the OS with SSH.

Original SSH account and password:

```
account: fysetc
password: fysetc123
```

Enter DFU mode(set a jumper on `3.3V` and `BOOT0` pin and re-power on the board ), and flash the firmware with the command below after you connect your OrangePi and S6 with USB cable.

```
dfu-util -R -a 0 -s 0x08008000:leave -D firmwares/s6.bin
```

or follow the instructions [here](https://github.com/FYSETC/FYSETC-SPIDER#44--firmware-upload) for firmware uploading. 

Remember to remove the `3.3v` `BOOT0` jumper and click the reset button after you flashed the firmware. 

![](OrangePi-zero\S6.jpg)

### Step 3:

Prepare the `pinter.cfg`, using the command below

```
cp klipper_config/s6-v2.cfg klipper_config/printer.cfg
```

You probably need to change `id` by `ls /dev/serial/by-id` command.

I use the generic config for this example, you need to change the config according to your machine. Now visit the webpage with your orangepi-zero IP address. Good to go.
