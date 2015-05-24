---
layout: post
title:  "Linux Command Tricks"
date:   2015-05-23 22:40:00 -0400
categories: Ubuntu
---

# 1. How to Schedule a Linux Job Without Cron


`$ while true; do date >> date.txt ; sleep 5 ; done &`


**Anatomy of the above one liner script:**

**while true** – Ask script to run while the condition is true, it acts as a loop which makes the command to run again-and-again or say in a loop.
**do** – do perform what follows, ie., execute command or set of commands that lies ahead of do statement.
**date >> date.txt** – here the output of date command is being written to a file date.txt. Also note that we have used >> and not >.
>> ensures that the file (date.txt) is not overwritten every time the script execute. It just append the changes. Whereas > overwrite the file again and again.
**sleep 5** – It ask the shell to keep a time difference of 5 seconds before it executed again. Note the time here is always measured in seconds. Say if you want to execute the command every 6 minutes, you should use (6*60) 360, in succession of sleep.
**done** – marks the end of while loop.
**&** – Put the whole process in loop to background.
Similarly, we can execute any script in the same manner. Here is the command to call a script after certain interval (say 100 sec) and the name of script is script_name.sh.

Also worth mentioning that the script above should be run in the directory where the script to be called lies, else you need to provide full path (/home/$USER/…/script_name.sh). The syntax for calling script at above described interval is:

`$ while true; do /bin/sh script_name.sh ; sleep 100 ; done &`
Conclusion: The above one liner is not a replacement of Cron, because Cron utility supports a whole lots of options, as compared and is very flexible as well as customizable. However if we want to run certain test cases or I/O benchmark, then the above singe command will serve the purpose.

# 2. Run a command and come back to the current working directory automatically.

Well this is an amazing hack not many people know. You may run a command no matter what it return back to the current directory. All you need to do is to run the command in parentheses i.e., in between ( and ).

*Let see the example,*

`avi@deb:~$ (cd /home/avi/Downloads/ && ls -l)`

*Sample Output*

	-rw-r-----  1 avi  avi     54272 May  3 18:37 text1.txt
	-rw-r-----  1 avi  avi     54272 May  3 18:37 text2.txt
	-rw-r-----  1 avi  avi     54272 May  3 18:37 text3.txt
	avi@deb:~$


[Credits](http://www.tecmint.com/)

[More](http://www.tecmint.com/11-cron-scheduling-task-examples-in-linux/)