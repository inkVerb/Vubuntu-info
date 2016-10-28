Ubuntu bases its time off of UTC, closer to the essential operation of your system, so you stay to date if you move and for daylight saving.

Windows writes it locally to your computer and manages the time zone through its own servers.

Windows' method is a bit more nanny-ish, Ubuntu's is more straight forward. But, they confuse each other and Windows won't know what time it really is with the more self-reliant Ubuntu installed on the same machine.

Here are some articles that explain what to do, which are the basis for this redaction, in order of simplicity:

http://www.webupd8.org/2014/09/dual-boot-fix-time-differences-between.html

http://askubuntu.com/questions/169376/clock-time-is-off-on-dual-boot

https://help.ubuntu.com/community/UbuntuTime#Multiple_Boot_Systems_Time_Conflicts

It is best to fix the problem in Windows:

1. Create "WindowsTimeFixUTC.reg" with this in it:
(or here: https://github.com/inkVerb/Vubuntu/blob/master/verbs/fixWindowsTime/WindowsTimeFixUTC.reg)

`Windows Registry Editor Version 5.00`
`[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\TimeZoneInformation]`
`     "RealTimeIsUniversal"=dword:00000001`
     
2. Double click on it in Windows

3. Run command prompt as admin and type this:

`sc config w32time start= disabled`

Un-change Windows:

1. Create "WindowsTimeFixUTC.reg" with this in it:
(or here: https://github.com/inkVerb/Vubuntu/blob/master/verbs/fixWindowsTime/WindowsTimeUnFixUTC.reg)

`Windows Registry Editor Version 5.00`
`[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\TimeZoneInformation]`
`     "RealTimeIsUniversal"=-`

2. Run command prompt as admin and type this:

`sc config w32time start= demand`
