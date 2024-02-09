Assignment 7b:

Ubuntu Version:	Ubuntu 16.04.7
Kernel version:	4.15.0-142-generic


Execution instructions:


1. Compile the assignment7b:

make

2. Load the usbkbd.ko

sudo insmod ubkbd.ko

3. Plug in the keyboard

4. Unbind the hid and bind the kbd

sudo bash -c "echo -n 2-2:1.0 >/sys/bus/usb/drivers/usbhid/unbind"
sudo bash -c "echo -n 2-2:1.0 >/sys/bus/usb/drivers/usbkbd/bind"

5. Unload the driver

sudo rmmod usbkbd

6. "make clean" to remove the files

