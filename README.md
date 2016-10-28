# Vubuntu™
## Ubuntu + inkVerb
*Settings, installs, and files for _ubuntu*
Vubuntu is NOT: [desktop environment] + Ubuntu ...which makes it special.

### About Vubuntu™
Vubuntu™ is an Ubuntu extension project with three parts:

1. Verber™: Web server scripts
2. Vrk™: Local workstation (desktop, notebook, tablet, etc.) with scripts and to link easily to a Verber™ server
3. Vubuntu™ desktop (scripts to install commonly used apps and settings on your workstation.)

#### Verber™ Web/Email server "cloud control" app engine for hosting
This part of the project contains several bash scripts called "serfs" that automatically set parameters, install, control, and manage web apps from the command line. Each serf contains instructions within the file.
Automating "cloud control" work on the hosting server speeds up work and reduces human error.
- Verber™ can be installed from the separate verber repository of inkVerb on GitHub.

##### Features
- Email, web app hosting, all on one, simple server. (Of course you can have multiple servers.)
- Easily host domains on the same server.
- Convenient for copywriters to manage multiple or individual clients, DIY (do it yourself) entrepreneurs, tech nerds who want to drive a 5-speed, and people who want ownership and control of their own cloud.
- The entire server can theoretically be duplicated on your home computer or another "controllable" web server. So, your stuff in the cloud is really, truly yours.
- Letsencrypt Certbot, of course.
- Apps currently include a Postfix/Dovecot server, PostfixAdmin, RoundCube, WordPress (with recipies!), ownCloud, SuiteCRM, OrangeHRM, Fossil-SCM, phpMyAdmin, Ghost, Ampache, SFTP accounts, net2FTP, and lots more to come!

##### Dependencies
- inkVerb™ namespace: subdomain for verb.ink, verb.email, verb.one, verb.blue, verb.guru, verb.kiwi, verb.red (available for $12/year, the Verber™ serfs use these to sort-out and access different apps, each domain can be a different server at the same price!)
- An in-app repository from inkVerb to install approved versions of some open-source apps (inkVerb™ handles this)
- A "controllable" web server, (not cute or 'unlimited' hosting from a cheap hosting provider) with the ability to install your own features, run scripts on the server, and manually edit settings files such as PHP, Apache, etc. inkVerb™ uses DigitalOcean ;-)

##### Notes
- You may modify these scripts for your own use, of course, remake it so it does not depend on "verb" domains or the inkVerb repository. This is part of the open license.
- You do not need to write the "TM" ™ after our words like we do, we're just watching out for the sharks. :-)
- You can support the project by purchasing an inkVerb™ namespace, which will point to the IP on whatever server you choose, including MX and TXT records (for OpenDKIM), or while the project is in Beta you need to choose your own DNS to manage the DNS records yourself.

#### Vrk™ workstation
The work station side of this project contains install scripts, links, and desktop backgrounds for humans computing at home and office.
Vrk™ (pronounced 'verk' as in 'work') contains several scripts to perform jobs and settings that normally require a little more knowledge than the average user knows.

It creates that extra "Work" folder everyone has a different name for, syncs "Documents" in your cloud across devices so you'll actually use it, lets you add your own wallpapers to the "official" selection list, and a lot more.

##### How to install:
Clone the vrk repo to your home folder and run vrk/inst/setupvrk, like this:

1. Install _ubuntu
2. Get the known universe moving
`sudo apt install git`
`cd ~`
`git clone https://github.com/inkVerb/vrk.git`
`cd vrk/inst`
`sudo ./setupvrk`

##### Vrk™ feathres:
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

#### Vubuntu™ Desktop
It was inspired by demand for "Kubuntu Studio", but why limit it to KDE? Vubuntu is your V-6, under the hood, getting the engine ship-shape no matter which desktop environment you want... GNOME, Unity, Xfce, KDE, Mint...

##### How to install:

1. Install Vrk (above)
2. ...
`cd .vrk/surf`
`sudo ./installvubuntu`

##### What "is" it?
*Vubuntu Desktop* has an installer included with Vrk™. It is not an "environment"; it's a set of install scripts that does what most users might do anyway for the first two or three hours after installing Ubuntu, all automated. If you have a cloud folder in your /home folder, after installing Vrk™ and Vubuntu Desktop, you might be all set to go.

Vubuntu includes some desktop themes and wallpapers, mostly minimalist for studios and in the booth.

It detects your environment and makes some no-brainer "Tweaks" in Unity, Xfce, and GNOME to make them less unbearable (in order of unbearableness,) but is more hands-off for KDE, Mint, and the rest (since those users tend to be more opinionated.)

Alt + rClick to resize windows, default dark minimal themes and flat icons, simple "creative space" wallpapers from inkVerb and Ubuntu Studio, Docky and Guake on startup... it's all setup.

One really cool thing: Vubuntu sets a "root" theme. So, when you sudo a desktop app, i.e. sudo nautilus, it looks a bit Valley-ish. root changes the prompt, it should change the theme also.

##### Types of features installed (may vary)
- Chromium, Docky, FileZilla, Midori, Epiphany Browser (if you have GNOME) Guake (with Indicator), Gedit, Libre Office, fonts galore, GIMP (with plugins), Inkscape, Audacity (with Chris' compressor), Audio Tag Tool, LMMS, Ardour, Blender, Darktable, Kdenlive, Flash, GNOME and Ubuntu Studio desktop goodies, Clementine, Amarok (most podcast-friendly), VLC (and friends), Stellarium, Dropbox, Skype, Linux low-latency, and tools like GParted, git, vim, zip, 7zip, etc.
- The above apps, and a few more, are installed in small clusters in case you have slow Internet and can't download it all in one session.
- Interactive install packages (MS fonts & Jackd) run first so you can quickly agree to EULA and settings, then walk away.
- It runs a script to automatically make icons visible in menues for Ubuntu (Unity) and GNOME.
- It automatically adds a Docky dock and Guake for startup, already configured
- You might consider installing Vubuntu™ before installing Ubuntu Studio, if you want to install all of Ubuntu Studio. Since many larger apps are included in Vubuntu™ Desktop, your Ubuntu Studio install time will be shorter.
- Planned: Vubuntu™ eventually plans to be an easily-installed Ubuntu distro that could be installed via unetbootin & USB.

inkVerb is not associated with Canonical, but Canonical is awesome anyway.
