Wget status:

If you're downloading with wget, you can simply check if the instance is still running:

ps -ef | grep wget | grep -v grep
Also, you could check whether the file is still opened by wget. Obviously, replace the path here.

lsof /path/to/downloaded/file


http://www.binarytides.com/better-elementary-os-luna/
