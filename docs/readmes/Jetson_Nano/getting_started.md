# Jetson Nano Guide for Absolute Beginners

???+ info inline end 
    This guide is typically for NVIDIA Jetson Nano Developer Kit 4GB


???+ info inline end
    Jetson Nano is a small and powerful micro-computer for AI and IoT applications


## Pre-install

Before installing your nano, you have to prepare for some stuff first.

### Physical Components

- [x] Micro-SD, recommend 32 Gb at least
- [x] Adapter/Power Supply 5V/(2A at least) [ jack or micro-usb type b ]
- [x] Monitor
- [x] Mouse & Keyboard or remote control keyboard
- [x] SD-card reader
- [ ] HDMI to VGA if your monitor doesn't support HDMI (optional)


???+ tip
    For future use, with heavy load, it is recommended to use the jack power (5V - 4A)


???+ tip
    You may use your mobile charger for the setup, if it meets the minimum requirements (5V and >= 2A)

???+ Danger
    Never use higher voltage. Yet, it is OK for higher current



## Software Components
- [x] OS image (you can find it [here](https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit#write))
- [ ] Prior Knowledge of Linux (optional)

## Burn the OS Image

We have two different options. Either via command line (which I prefer), or via Etcher

### Etcher

<!-- fix here and stackoverflow -->

Etcher is well-explained [here]() (I recommend reading this, if you prefer GUI)

### Command Line

- Check device name by inserting the SD-card and typing `sudo fdisk -l` in your terminal
- Now, eject the device and notice which device isn't available now (obviously, the SD-card)
- Unmount the partitions by `sudo umount <device-name>`
- `sudo dd bs=1M if=your_image_file_name.img of=/dev/<device-name>`

<!-- I have tried to use my mobile phone as a reader. Yet, it didn't work. So, please make sure you have a reader. ( I had to buy one for it)
 -->

???+ Note
    I have tried to use my mobile phone as a reader. Yet, it didn't work. So, please make sure you have a reader. ( I had to buy one for it)



## The Real Installation

1. Insert your SD-card into your Jetson Nano (the slot is a lit bit tricky)
2. Connect whatever peripherals you may need (keyboard, mouse, and monitor)
3. Plug the power, and voila

![](../../assets/nano/jetson_1.webp)

???+ Tip
    I'm using wireless mini keyboard to lessen the power load over my Jetson Nano

1. You may observe the OS is booting. Wait until the welcome page is there

![](../../assets/nano/jetson_2.webp)

<br>

???+ Tip
    The setup may take long time (> 3 hrs). You may then need to reboot the device and restart the setup




1. Once this is done, just select the default parameters and let the setup work by itself

![](../../assets/nano/jetson_3.webp)
![](../../assets/nano/jetson_4.webp)
![](../../assets/nano/jetson_5.webp)
![](../../assets/nano/jetson_6.webp)

Finally, it asks you to restart. Restart

![](../../assets/nano/jetson_7.webp)
