---
title: My setup and hardware
layout: home
nav_order: 6
---


# My setup and Hardware

I recently change my approach to use containers instead of Home Assistant VM for the following reason:
- My home assistant take more than 5 mins to restart all the extension etc..
- Restart the VM and Home Assistant take more than 15 mins
- There is update every week ( I want to keep up but I don't have 1h to reserve every week for update in case something goes wrong and I need to use a backup)
- If home assistant crash during update/restart EVERYTHING stop

With container I separate Home Assistant,Node-Red,Zigbee2MQTT,Emqx & MariaDB.
- I'm using [mqdockerup](https://github.com/MichelFR/MqDockerUp) for update notification and update
- Restart one container for update take less than a minute ( And I will find a way so it take less than a second even for Home Assistant 😄)
- I use Zigbee over ethernet so I'm not relying on USB stick.

So today, I'm running Home Assistant, Node-Red, Zigbee2Mqtt, Emqx and MariaDB in docker container on my Synology DS920+ (with additional SSD and 20Go of RAM)

The Wall Mount tablet is a FireHD 10 from amazon running Fully Kiosk Browser.
