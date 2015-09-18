---
layout: post
title:  "nVidia black screen fix for Ubuntu on Macbook Air"
date:   2015-05-25 05:20:00 -0400
categories: Ubuntu
---

#Nvidia driver blank/black screen crash

After installing ubuntu/debian-based distros in Macbook Air 11" Late 2010, if we install nvidia driver manually from Terminal or if some other applications which have dependency on nVidia graphics driver(tends to update the driver when they install) causes the black screen problem.

This will be found only at the time of reboot.

There is a quick and easy way to fix this issue:

1. Power on the system and press 'Esc' once while you hear the 'chime' sound.
2. You will either see the 'grub menu' or 'grub>'
3. If you see grub menu then select the (recovery mode) to boot from.
4. if you see the grub>> then hold power button and redo the steps from 1 (But this time instead of 'Esc' press 'Esc' and 'Shift' separately.
5. Once you boot into the recovey mode, you will see few options to select
6. Now select "Drop to root shell prompt"
7. Type the following commands to remove nvidia driver completely and reboot.
`sudo apt-get remove --purge nvidia-*`
`reboot`


This time you will not be blocked by the black screen.

[Source](http://ubuntuforums.org/showthread.php?t=2209602)
