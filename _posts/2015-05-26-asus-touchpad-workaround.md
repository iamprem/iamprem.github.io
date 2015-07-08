---
layout: post
title:  "Asus Touchpad Workaround in Ubuntu"
date:   2015-05-26 23:45:00 -0400
categories: ubuntu
---

## Asus Touchpad Workaround in Ubuntu

1. Boot into ubuntu and open terminal
2. Run the following command
`sudo gedit /etc/default/grub`
3. Find the line `GRUB_CMDLINE_LINUX_DEFAULT="quite splash"`
4. Add psmouse.proto=bare at the end of the "quite splash" parameter followed by a space
5. Run sudo update-grub to update
6. Reboot the machine.

Done!!

