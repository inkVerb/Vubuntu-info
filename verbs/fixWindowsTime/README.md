Ubuntu bases its time off of UTC, closer to the essential operation of your system, so your machine's time stays to date if you move or daylight saving time happens in your sleep.

Windows writes it locally to your computer and manages the time zone through its own servers.

Windows' method is a bit more nanny-ish, Ubuntu's is more straight forward. But, they confuse each other and Windows won't know what time it really is with the more self-reliant Ubuntu installed on the same machine.

Here are some articles that explain what to do, which are the basis for this redaction, in order of simplicity:

http://www.webupd8.org/2014/09/dual-boot-fix-time-differences-between.html

http://askubuntu.com/questions/169376/clock-time-is-off-on-dual-boot

https://help.ubuntu.com/community/UbuntuTime#Multiple_Boot_Systems_Time_Conflicts

It is generally advisable to fix the problem in Windows. Fixing it in Ubuntu is easy, but daylight saving and time updates will break, making you the Ubuntu nanny while Windows nannies herself. This may not work in "older" versions of Windows. Read the above articles for the scoop. Here is inkVerb's Digest version:

# Fix the problem in Windows:

Create "WindowsTimeFixUTC.reg" with this in it:

`Windows Registry Editor Version 5.00`
`[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\TimeZoneInformation]`
`     "RealTimeIsUniversal"=dword:00000001`

(or download here: https://github.com/inkVerb/Vubuntu-info/blob/master/verbs/fixWindowsTime/WindowsTimeFixUTC.reg)

1. Double click on WindowsTimeFixUTC.reg in Windows

2. Run command prompt as admin and type this:

`sc config w32time start= disabled`

# Un-fix the problem in Windows:

Create "WindowsTimeUnFixUTC.reg" with this in it:

`Windows Registry Editor Version 5.00`
`[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\TimeZoneInformation]`
`     "RealTimeIsUniversal"=-`

(or download here: https://github.com/inkVerb/Vubuntu-info/blob/master/verbs/fixWindowsTime/WindowsTimeUnFixUTC.reg)

1. Double click on WindowsTimeUnFixUTC.reg in Windows

2. Run command prompt as admin and type this:

`sc config w32time start= demand`

...Everything above is at your own risk. Then, again, so is using Windows.
