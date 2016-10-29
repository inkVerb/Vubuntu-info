# Vubuntu™
## Ubuntu + inkVerb
*Settings, installs, interface, and cloud control for _ubuntu*

### Note:

Vubuntu is NOT: [desktop environment] + Ubuntu ...which makes it special.

Vubuntu Desktop and Vubuntu Studio Lite are installed via the "inkVerb/vrk" repo. This for information, related how-to scripts, and *the future...*

inkVerb and Canonical are NOT associated, but Canonical is awesome anyway.

### About Vubuntu™
Vubuntu™ is an Ubuntu extension project with three branches:

1. Vrk™ Station: Local workstation (desktop, notebook, tablet, etc.) to easily link and control a Verber™ Server
2. Vubuntu™ Desktop: Cloud control for humans (scripts to install commonly used apps and settings on a workstation.)
3. Verber™ Server: Controllable cloud (LAMP server with scripts for routine tasks)

#### 1. Vrk™ Station
The local work station side of this project contains install scripts, links, and desktop backgrounds for humans computing at home and the office. You don't need a Verber for your Vrk Station to control, *but you want one...*

Vrk (pronounced 'verk' as in 'work') contains several scripts to control jobs and settings that normally require a little more knowledge than the average user has and can take a lot more time than any webmaster has. A Verber has "serf" bash scripts for its kingdom, a Vrk Station is more down to earth and calls them "surfers".

Vrk creates that extra "Work" folder everyone has a different name for, syncs "Documents" in your favorite cloud across devices so you'll actually use it, lets you add your own wallpapers to the "official" selection list, and a lot more.

##### How to install:
Clone the vrk repo to your home folder and run vrk/inst/setupvrk, like this:

1. Install your Ubuntu distro
2. Ctrl + Alt + T

`sudo apt install git`

`cd ~`

`git clone https://github.com/inkVerb/vrk.git`

`cd vrk/inst`

`sudo ./setupvrk`

##### Vrk™ features:
- Automatically links home folders "Documents", "Templates", and your own custom folder to a cloud folder of your choice: Dropbox, ownCloud, Pydio, or another cloud service that uses a simple directory. Vrk™ carefully moves contents to the cloud, merges any content, then replace these user home folders with links. This way, your home folders can be synced to your choice cloud across devices.
- Vrk™ includes a "Templates" folder with some common starter documents and files.
- It has scripts to quickly add Guake Indicator profiles, SSH keys and credentials, and install the lated ownCloud with repos
- Vrk™ can be installed from the separate inkVerb/vrk repository of  on GitHub.
- Vrk™ is used to install the Vubuntu Desktop.

##### .vnk/.vink file type (beta)
- The .vink file extension is an empty file that you can train your operating systems to open with a simple text editor or Dropbox can easily export to a text editor.
- Generally, .vnk is created and used locally while .vink is used on a Verber™ server or another web app. But they can be used interchageably much like .htm and .html.
- A .vnk file can be read as an html file with the <!DOCTYPE html> declaration as a solution for rich text. 
- .vink is part of a roadmap for a "post / email" file that can be recognized as either html, simple text, or markdown. A .vink-powered CMS may store posts and/or emails and/or notes as .vink files on the server rather than as database entries.
- Planned: .vink files to recognize a word followed by ampersand, ie: word& , as an "anchor" and a word followed by hash, ie: word# , as a link to it. Double and tripple ampersand and hashes should render as superscript and subscript, respectively. And a single, double, or tripple may be trailed by an i, b, u, or any combo thereof for italics, bold, or underlined styling of links and anchors. Links and anchors can be given a longer name via: [Longer Name of Link]link&. This promotes non-conflicting serchability via a mod to markdown's style. Trailing hashes and ampersands are not known to be used elsewhere.
- Planned: "!" to double for a subdomain "dot" and an email address "@", depending on applied usage. This is for your-name!verb.ink customers.

#### 2. Vubuntu™ Desktop
It was inspired by demand for "Kubuntu Studio", but why limit it to KDE? Vubuntu is your V-6, under the hood, getting the engine ship-shape no matter which desktop environment you want... GNOME, Unity, Xfce, KDE, Mint...

##### How to install:

1. Install Vrk (above)
2. Ctrl + Alt + T

`cd .vrk/surf`

`sudo ./installvubuntu`

##### What "is" Vubuntu™ Desktop?
*Vubuntu Desktop* is included with Vrk™. It is not an "environment"; it's a set of install scripts that does what most users might do anyway for the first two or three hours after installing Ubuntu, but it's all automated.

Vubuntu Desktop includes desktop, theme, and wallpapers settings, mostly minimalist for studios and in the booth. It includes the "Vubuntu Studio Lite" toned-down recipe of Ubuntu Studio apps and common desktop tools.

Vubuntu Desktop detects your environment and makes several no-brainer "Tweaks" in Ubuntu (Unity), and just a few in Xfce and GNOME, to make them less unbearable, but is more hands-off for KDE, Mint, and other environments that cater to GUI connoisseurs.

Alt + rClick to resize windows, default dark minimal themes and flat icons, simple "creative space" wallpapers from inkVerb and Ubuntu Studio, Docky and Guake on startup... Vubuntu automatically makes icons visible once again in menues for Unity and GNOME. It can even set a "root" theme, so, when you sudo a desktop app, i.e. sudo nautilus, it looks different from all other windows... It's all set up for you by Vubuntu Desktop's install script. If you have a cloud folder and a USB with former Ubuntu settiongs (Vrk backs those up to USB also,) after installing Vrk™ and Vubuntu Desktop, your _ubuntu installation will be setup in a snap.

Ink is a verb. So, don't waste time fixing OOB settings. Vrk will do the work so you can get inking.

(out of box)

##### Vubuntu™ Studio Lite apps

- Chromium, Docky, FileZilla, Midori, Epiphany Browser (if you have GNOME) Guake (with Indicator), Gedit, Libre Office, fonts galore, GIMP (with plugins), Inkscape, Audacity (with Chris' compressor), Audio Tag Tool, LMMS, Ardour, Blender, Darktable, Kdenlive, Flash, GNOME and Ubuntu Studio desktop goodies, Clementine, Amarok (most podcast-friendly), VLC (and friends), Stellarium, Dropbox, Skype, Linux low-latency, and tools like GParted, git, vim, zip, 7zip, etc.
- The above apps, and a few more, are installed in small clusters. In case you have slow Internet and can't download it all in one session, you can pick up closer to where you left off.
- Interactive install packages (MS fonts & Jackd) run first so you can quickly agree to EULA and settings, then walk away.
- Installing Vubuntu Desktop's "Studio Lite" first makes Ubuntu Studio install more smoothely. (Vrk has an Ubuntu Studio install script also, but doesn't change the desktop environment.)

##### Planned
Vubuntu™ eventually plans to be an Ubuntu distro that could be installed via unetbootin & USB. But, that is "very eventually".

##### Thoughts and backstory, from Jesse

GNOME is awesome for working at a desk, but it has issues: It doesn't handle large copy operations well, the top corner dash doesn't always work, and 64_ARM gives the same sluggish crash report on every startup. It's best for an old i386 in the shop where most of your projects actually happen.

Unity is a lot more stable than GNOME, and it's from Canonical and is intended for the OS. But if we wanted to look at the same ten icons all day we would use Windows, and "can't catch me" notifications exist nowhere else in the known metaverse—the Post Office, Gmail, mom, Xfce and all other Ubuntu desktops—all else lets you acknowledge messages, but not Unity. And gradiants require too much serotonin to look at while your counting pixels for a logo. The Vubuntu Desktop script fixed this.

Xfce, speaking of gradiants, is very VERY minimalist. So, it's ideal for work in the live booth. Dark desktop themes are good for that, enter Cyanogen inspired theming. (wink, grin) Graybird, Numix, and darkness is good OOB where stability via simplicity is a marketable need.

KDE, in short: Too much fiberglass on wooden chasis. They have the stability-pioneering balance of BMW, always in the fray. If it manages to be stable and play well with others, then there isn't really anything to change. But, it won't be in the live booth anytime soon... until the Antagonist loses his job trying to prove otherwise. Kubuntu has a lot of uses, beyond mom and the art class, which is why many of its settings are included in Vrk's USB backup settings script.

Mint was my first Ubuntu install back in the 13.04 days. Haven't done much since. But, its desktop is geared to work OOB. And, that's probably the main angle of most other distros. So, I don't mess.

###### You can add for other distros
I don't have time to try them all. I've been too busy inking. Feel free to pull-request a good setting script in the installvubuntu-desktop surfer for your favorite Desktop. If you have 1. the $DESKTOP_SESSION if test 2. stay within style and scope of the other desktop-specific settings, I will probalby include it. Note, only Unity gets so elaborate because only Unity needs to. If you think another desktop env should be included elaborately, tell me why in the notes and I'll learn from you.

#### 3. Verber™ Web/Email server "cloud control" app engine for hosting
This part of the project contains several bash scripts called "serfs" that automatically set parameters, install, control, and manage web apps from the command line. Each serf contains instructions within the file.
Automating "cloud control" work on the hosting server speeds up work and reduces human error.

##### How to install

1. Get your Ubuntu 16+ LTS VPS going, probably on Digital Ocean, NOT a LAMP server!
2. Get into your command line as root...

Note: make-verber-preserver, make-verber, and setupverb have instructions and examples at the start of each file. Use vim or nano to see them. They delete themselves after running because you only need them once.

`apt install git`

`cd /var/local`

`git clone https://github.com/inkVerb/verber.git`

`cd verb/inst`

`./make-verber-preserver`

`reboot`

Login again as root...

`cd verb/inst`

Choose the setting in brackets, "2" is probably good enough unless you have a reason to disagree...
`./make-verber [swap-size, choose GB: 1, 2, 4, 8, 16, 32, 64]`

Get these settings in brackets exact the first time. See longer description below...

`./setupverb [host] [namespace] [tld] [serverIP] [SSLemail] [php.file-limit] [php.up-size] [php.region] [php.city] [new-port] [new-boss] [boss-pass]`

Longer description for setupverb settings:

[host - should be namespace or FQDN tld, unless you want to be strange]

[inkVerb namespace (purchased)]

[FQDN tld, should be 'ink' except multiple servers for namespace]

[server IP]

[SSL email - used for Letsencrypt and the like]

[php file upload limit]

[php upload size in MB]

[php timezone region]

[php timezone city]

[new port number for ssh/terminal login]

[new "boss" sudo user]

[boss user password]

##### How to use:

See READ.ME

Then, use this cheat-sheet: https://github.com/inkVerb/Vubuntu/blob/master/Verber-overview.md

##### Features
- Email, web app hosting, all on one, simple server. (Of course you can have multiple servers.)
- Easily host domains on the same server.
- Convenient for copywriters to manage multiple or individual clients, DIY (do it yourself) entrepreneurs, tech nerds who want to drive a 5-speed, and people who want ownership and control of their own cloud.
- The entire server can theoretically be duplicated on your home computer or another "controllable" web server. So, your stuff in the cloud is really, truly yours.
- Letsencrypt Certbot, of course.
- Apps currently include a Postfix/Dovecot server, PostfixAdmin, RoundCube, WordPress (with recipies!), ownCloud, SuiteCRM, OrangeHRM, Fossil-SCM, phpMyAdmin, Ghost, Ampache, SFTP accounts, net2FTP, and lots more to come!

##### Dependencies
- inkVerb™ namespace: subdomain for verb.ink, verb.email, verb.one, verb.blue, verb.guru, verb.kiwi, verb.red, verb.rocks, verb.uno (available for $12/year, the Verber™ serfs use these to sort-out and access different apps, each domain can be a different server at the same price!)
- An in-app repository from inkVerb to install approved versions of some open-source apps (inkVerb™ handles this)
- A "controllable" web server, (not cute or 'unlimited' hosting from a cheap hosting provider) with the ability to install your own features, run scripts on the server, and manually edit settings files such as PHP, Apache, etc. inkVerb™ uses DigitalOcean ;-)

##### Notes
- You may modify these scripts for your own use, of course, remake it so it does not depend on "verb" domains or the inkVerb repository. This is part of the open license.
- You do not need to write the "TM" ™ after our words like we do, we're just watching out for the sharks. :-)
- You can support the project by purchasing an inkVerb™ namespace, which will point to the IP on whatever server you choose, including MX and TXT records (for OpenDKIM), or while the project is in Beta you need to choose your own DNS to manage the DNS records yourself.

##### Verber origin, from Jesse

Digital Ocean was doing their Google ad campaign back around 2014. I was tired of my registrar-host. The voice in my head said, "Give it a try." I was still expirimenting with Ubuntu on my Windows 8 book, the first of its kind. I didn't really have a reason for it all. Learning Ubuntu was just a matter of character. "Who I am" demanded that I try this particular thing that particular friends of mine talked about.

Needless to say, Ubuntu LAMP on Digital Ocean ran all my WordPress sites rather well. I started designing in a makeshift Xubuntu Studio install, since unetbootin couldn't do U-Studio on my machine. I started playing with ownCloud, as if I didn't have enough reasons for headaches. Buggy, but they are getting their vapors in a group. Eventually, I hit that epiphany moment when I realized that the file system on my notebook was the same on my Ubuntu server. That was just after I spend a week trying to get Ex Ratione's Postfix Admin - Roundcube email server working. I finally got it right and made a snapshot. A year Digital Ocean caught on and started billing for snapshots, smart them.

After a while, I realized there were many things I kept doing again and again. I didn't like taking an entire day to set up a "Hillarymail" server and risking one semi-colon messing everything up. That was when I started "bashing". It literally got me to a place where I won't make one, single change on my servers without writing a script to do it. They started piling up.

All the while this is going on, I thought, "I should write my own CMS editor. Rather than 'New post', I should just have a pen and call the hover 'Ink.' Ink is a verb, after all." Registrar search, verb.ink, and the rest was history.

As for all the little bash scripts that piled up—I put them in the "verb" directory. From there, it was an unintended construction site. By the time 16.04 LTS came out, I had fully automated the entire installation process for the entire server. One-command app installs, ownCloud, Pydio, WP, Ghost, Drupal, SuiteCRM, OrangeHRM, Ampache, Roundcube, PostfixAdmin, MediaWiki, who knows what else, and Letsencrypt just arriving on the scene... It was what every copywriter and entrepreneur needed.

The last step was to get a server-to-server system for internal SSL CA purposes, one-click spinups, and my own stable release channel. (Why don't most developers learn from WordPress and just have a "latest.zip" package with the version number in the READ.ME?) If I'm lucky, I'll be able to set up an SSL Cert Authority for servers using the Verber scripts. But, that's future.

The plan as of 2016 Q4 was to survive America's election and start on a GUI so more people can use what I spent two years unintentionally making on the backend. Thanks, Andy Bucher, for jabbering about Linux in high school. I'm sure we'll meet again in the clouds. In the meanwhile, I have some inking to get to.
