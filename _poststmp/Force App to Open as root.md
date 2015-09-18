

You can also go to /usr/share/applications in ubuntu and edit the launch file of the application you are trying to run.
Like i edited the file of github atom, normally i use a wildcard to find the files like this

sudo nano atom*

This will open the atom.desktop file, now find the Exec command and prepend gksudo.For eg.,

Before

Exec=/usr/share/atom/atom %U  

After

Exec=gksudo -k -u root /usr/share/atom/atom %U

Now whenever the application is launched it will ask for root password.
