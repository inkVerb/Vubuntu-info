# Vubuntu™
## Ubuntu + inkVerb scripts
*Settings, installs, and files for _ubuntu*

### About Vubuntu™
Vubuntu™ is an Ubuntu extension project with two parts:

1. Web servers (Verber™)
2. Local workstations: desktop, notebook, tablet, etc. (Vnk™)

#### Verber™ Web/Email server "cloud control" app engine for hosting
This part of the project contains several bash scripts called "serfs" that automatically set parameters, install, control, and manage web apps from the command line. Each serf contains instructions within the file.
Automating "cloud control" work on the hosting server speeds up work and reduces human error.

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

#### Vnk™ workstation
The work station side of this project contains install scripts, links, and desktop backgrounds for humans computing at home and office.
Vnk™ (pronounced 'vink' as in 'sink') can create cloud folders in Dropbox, ownCloud, or another cloud service, then replace user home folders with links. This way, your home folders can be synced to your choice cloud across devices.
- Vnk™ includes a Templates folder with some common starter documents including .vnk (or .vink) files for txt files.
- The .vnk file extension is an empty file that you can train Dropbox or other operating systems to open with a simple text editor.
- A .vnk file can be read as an html file with the <!DOCTYPE html> declaration as a solution for rich text. 
- .vnk is part of a roadmap for a "post / email" file that can be recognized as either html, simple text, or markdown. A .vnk-powered CMS may store posts and/or emails and/or notes as .vnk files on the server rather than as database entries.
- Planned: .vnk files to recognize a word followed by ampersand, ie: word& , as an "anchor" and a word followed by hash, ie: word# , as a link to it. Double and tripple ampersand and hashes should render as superscript and subscript, respectively. And a single, double, or tripple may be trailed by an i, b, u, or any combo thereof for italics, bold, or underlined styling of links and anchors. Links and anchors can be given a longer name via: [Longer Name of Link]link&. This promotes non-conflicting serchability via a mod to markdown's style. Trailing hashes and ampersands are not known to be used elsewhere.
- Planned: "!" to double for a subdomain "dot" and an email address "@", depending on applied usage. This is for your-name!verb.ink customers.

#### Vubuntu™ also has other scripts for installing Ubuntu with many apps quickly.
These are scripts and copyable commands that may be useful for verbists and Ubuntu power users.
- guake-indicator is a guake addon that allows quick terminal access to other linux instances via command line.
- Other publishing tools are also included, borrowing many scripts from Ubuntu Studio, good work guys!
- vStudio contains copyable commands to finish installing extra apps quickly
- vubuntu-studio installs all these in one command
