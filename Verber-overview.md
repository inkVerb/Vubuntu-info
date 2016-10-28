This is markdown cheat-sheet of features and instructions for Verber from the inkVerb/verber repo.

Make sure you read the READ.ME file in inkVerb/verber all the way through. This cheat-sheet assumes you have.

This does not include everything possible, but addresses the majority

Everything is in /var/local/verb, with a link in the home folder, including root.

All jobs are in verb/serfs. Each serf has the purpose, instructions, and examples at the top of the file, use vim or nano to read them.

### Services

#### SSH, Users, & Server Maintenance
*See the .guru section for many more users*

`newboss` `rootloginoff`

`setufwip` `setport` `setswapsize` `showverber`

- For restoring from a snapshot:
`setlocale`

#### Email server

`installemail`/`setpfapass` `postinstallpfa`/`postinstallrc` 

`backupemail`/`backupemailrestore`

#### Domain management

##### Hosted domains

`newdomain`/`newdomaincgi`/`killdomain` `addsubdomain`/`addsubdomaincgi`/`killsubdomain` `changedomcgitodom`/`changedomtodomcgi` 

`pointdomain` `fixwww`

##### inkVerb namespace domains

`newgurusub`/`newgurusubcgi` `newonesub`/`newonesubcgi` `newunosub`/`newunosubcgi` `newverbsub`

`pointguru` `pointone` `pointuno` `pointink`

`verbon` `verboff`

#### MySQL

`mysqldbusr` `mysqlnewdb` `mysqlex`/`mysqlin` `mysqlnewboss` `mysqlboss`

#### .guru services
`newserverguru`

##### FTP
*This really is necessary for .guru services to be useful*

`installvsftpd`

`adddomainfiler` `activatefiles` `activaterepo` `newftpuser`/`killftpuser` `newftpfiler`/`adddomainfiler`/`killftpfiler` `newftpguru`/`killftpguru`

##### CGI

`installcgi` # Necessary to initiate

- Related

`activatecgi` # Turns cgi.YOU.verb.guru on and off

##### Fossil SCM

`installfossil`

`newfossil` `newfossiluser` `newfossilpass`

### Web Apps

#### Verber app management
`backup` `backuprestore`/`backuprestoreowncloud` `killvapp`

### .ink, domains

#### WordPress

`wpadd` `wpautoupdateoff` `wpsecure` `wplinkdomain`/`wpunlinkdomain`

- For domains

`installwp` 

- For .ink blogs

`installwpinkbb` `installwpinkblog`

#### Drupal

- For domains

`installdrupal`

- For .ink blog
`installdrupalinkblog`

- Browse available included distros
`showdrupaldistroes`

#### Ghost

- For domains

`installghostsite`

- For .ink blog

`installghostinkblog`

#### Ampache
.kiwi
`installampache` `ampachepodcast`

#### ownCloud
.blue

#### Pydio
.blue

### .red
#### SuiteCRM

`postinstallscrm`

#### OrangeHRM


### inkVerb special service
These have a flow of their own, are generally used as dependencies, and you should follow their flow to learn more

#### inkCert

#### inkNet


