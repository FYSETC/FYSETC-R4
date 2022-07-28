# OS

## SAMFi-OS_OrangePi_zero

Before you config the SAMF-OS_OrangePi_zero. You need an TF card with at least 8G capacity.

### Step 1

Download and flash the OS image with `balenaEtcher` software to your TF card. Insert your flashed TF card to OrangePi-zero and connect Ethernet cable then power on. Find the ip address of OrangePi-zero on your router, host name is `orangepizero`.

![](OrangePi-zero\OrangePi_zero.jpg)

### Step 2

You can find the firmware `klipper.uf2` in `OrangePi-zero` folder after you download the github repository. It is also stay in the OS path `firmwares\r4.bin` after you login the OS with SSH.

Original SSH account and password:

```
account: fysetc
password: fysetc123
```

follow the instructions [here](https://github.com/FYSETC/FYSETC-R4#firmware-upload) for firmware uploading. 

![](OrangePi-zero\R4.jpg)

### Step 3:

Prepare the `pinter.cfg`, using the command below

```
cp klipper_config/r4.cfg firmwares/printer.cfg
```

You probably need to change `id` by `ls /dev/serial/by-id` command.

I use the generic Klipper config for this example, you need to change it according to your machine. Now visit the webpage with your orangepi-zero IP address. Good to go.
