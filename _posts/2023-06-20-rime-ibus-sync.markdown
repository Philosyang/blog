---
layout: post
title:  "Rime cloverpinyin on Ubuntu with cloud dict sync"
date:   2023-06-20 20:43:00 -0500
categories: linux rime
---
This is more like a self note so that I can quickly set up future linux instances.

I'm playing with ubuntu recently. Windows 11 made me want to roll back to windows 10 except that I made too many registry changes and tweaks that I just want to ditch Windows altogether.

With Steam making Proton, as well as Apple creating the "Porting Toolkit" (Proton-like) tool that enables Macs to run Windows games, I think that we will be able to game easily on linux in the near future.

[ibus-rime](https://github.com/rime/ibus-rime) let's me type 中文 with Rime in linux. 

install: https://github.com/rime/home/wiki/RimeWithIBus

[🍀四叶草拼音 input schema](https://github.com/fkxxyz/rime-cloverpinyin)

[🍀四叶草拼音 installation on linux](https://github.com/fkxxyz/rime-cloverpinyin/wiki/linux)

for ~/.config/ibus/rime/installation.yaml:

installation_id is used to identify each Rime instance, I usually do my computer's name + OS name.

sync_dir is used to let Rime copy all user config to this sync_dir so that we can easily use methods (cloud sync) to sync user configs and dicts; I use MEGA so my sync_dir is 'MEGA/keys/settings/Rime' (there are many installation_id folders under this Rime folder, each represents a Rime instance (e.g., my laptop, my pc with windows os, etc.))

Everything works! I will try to figure out how to let Rime auto-sync in ubuntu in the future. (In Windows I created a task under task scheduler that runs sync when computer is idle)
