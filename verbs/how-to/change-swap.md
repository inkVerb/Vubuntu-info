# Chane swap UUID in fstab

Linux must know the UUID of swap, which changes when you remake a partition. If you remake your swap partition after installing, Linux will be confused and take a long time to start up.
*(You'll be looking at that pretty graphic called a 'Plymouth' forever at every boot up.)*

1. Get a list of your partitions:

`sudo blkid`

*Look at the list and find* TYPE="swap" *with* UUID="ab20cd31ef42-some-long-number"

2. Open a GUI editor with GUI password entry (because GUI is easy and kind of the point)

`gksu gedit /etc/fstab`

Note:
- `gksu` is like `sudo`, but for GUI.
- `gedit` is the editor.
- `/etc/fstab` is the settings file.

*If you don't have* `gedit`*, you can use* `mousepad` (Xfce) *or* `kate` (KDE) *or* `pluma` (MATE/Cinnamon) *or whatever else instead. Nothing is stopping you from using* `vim` *or* `nano` *in the terminal either.*

Now, look at the `/etc/fstab` file that opened in the GUI. It has the swap UUID two times, the first was swap at install, usually "ext4" and not "swap". Later is the actual swap. Change the actual one.

Copy that long UUID number for swap from the terminal (Ctrl+Shift+C for terminal) and use that to replace the UUID swap number in `/etc/fstab`.

Save & close.

All is good and right in the world at next boot.
