---
templateKey: blog-post
title: Identifying Bird Species with the Sound of their Calls and Songs.
date: 2022-05-31T17:34:24.630Z
description: Ever heard the sound of a bird on your roof, or you've always
  wondered; what is that bird that wakes me up every morning? With this simple
  and easy-to-setup project running on a Raspberry Pi, you'll be able to find
  out in a matter of seconds. Here's how!
featuredpost: true
featuredimage: /img/fa1c3e9f-acdb-4cfb-9411-0b52bf6b3aba.png
tags:
  - raspberrypi
  - birdnetpi
---
## Ok, let's get started.

### Here's what you'll need:

* Raspberry Pi (4B, 3B(+) or Zero W 2, but other untested versions may work too)
* SD Card
* USB Microphone or Sound Card
* A Wired or Wireless Internet Connection (wireless will need to be set up beforehand in the Raspberry Pi Imager options)
* A Power Cable (preferably one that came with your Pi)
* An existing computer

#### Optional:

* A case for your Raspberry Pi
* A fan and/or heatsinks for your Pi

Here's what all my equipment looks like:

![all of the equipment](/img/img_20220531_092835.jpg)

And I've set up my microphone next to an open window like this:

![microphone pointing out of an open window](/img/img_20220531_093512.jpg)

### Once you have these hooked up, head over to a working computer to set up your SD Card:

I used the Raspberry Pi Imager to flash my OS onto my SD Card. Head over to the official [Raspberry Pi Website](https://www.raspberrypi.com/software/) or use these direct download links to get the imager:

* [Raspberry Pi Imager for Windows](https://downloads.raspberrypi.org/imager/imager_latest.exe)
* [Raspberry Pi Imager for Mac](https://downloads.raspberrypi.org/imager/imager_latest.dmg)
* [Raspberry Pi Imager for Debian Linux x86 (e.g. Ubuntu)](https://downloads.raspberrypi.org/imager/imager_latest_amd64.deb)

Once installed, launch the imager if you haven't already, then proceed to choose Raspberry Pi OS Lite (64-bit) as the operating system and your SD Card as the target device. Then, make sure to choose the option to enable SSH and set a password. Additionally, if you're planning to use Wi-Fi, enter the credentials for it on the same settings page.

<iframe width="560" height="315" src="https://www.youtube.com/embed/koGzeACPeO4?controls=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

After your SD Card has finished being written to and verified, go ahead and pop it into your Raspberry Pi and power it up. Wait a couple minutes for your Pi to boot up, then head back to your computer. Open up your terminal or command prompt and SSH into your Pi by running `ssh pi@ip.address`, replacing "ip.address" with the IP address of your Pi. You can find this out either by attaching a monitor to it and running `ifconfig`, or by guessing it. For example, on any new setup with an ethernet cable attached, my Raspberry Pi's IP address is always set to 192.168.1.225, so it might be worth trying that. If it's your first time connecting, you might need to type yes to accept the fingerprint and continue. Once you're in, you'll be ready to run the main command which will download and install BirdNet-Pi, along with any prerequisites it may need. Are you ready? Here it is: `curl -s https://raw.githubusercontent.com/mcguirepr89/BirdNET-Pi/main/newinstaller.sh | bash`

##### When the installation is complete, head over to [birdnetpi.local](birdnetpi.local) in your web browser.

## **And that's all! Your Pi should now be picking up sounds and telling you what type of bird it is. Have fun and don't be afraid to explore!**