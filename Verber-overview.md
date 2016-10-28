This is markdown cheat-sheet of features and instructions for Verber from the inkVerb/verber repo.

Make sure you read the READ.ME file in inkVerb/verber all the way through. This cheat-sheet assumes you have.

This does not include everything possible, but addresses the majority

Everything is in /var/local/verb, with a link in the home folder, including root.

All jobs are in verb/serfs. Each serf has the purpose, instructions, and examples at the top of the file, use vim or nano to read them.

### Services

#### Email server

- Do all of it at once:

`installemail`

#### Domain management

##### Hosted domains

##### inkVerb namespace domains

#### .guru services

##### FTP
*This really is necessary for .guru services to be useful*

`installvsftpd`

- Related

`adddomainfiler` `activatefiles` `activaterepo` `newftpuser`/`killftpuser` `newftpfiler`/`adddomainfiler`/`killftpfiler` `newftpguru`/`killftpguru`

##### CGI

`installcgi` # Necessary to initiate

- Related

`activatecgi` # Turns cgi.YOU.verb.guru on and off

##### Fossil SCM

`installfossil`



### Web Apps

#### WordPress
.ink, domains

#### Drupal
.ink, domains

- For domains

`installdrupal`

- For .ink blog
`installdrupalinkblog`

- Browse available included distros
`showdrupaldistroes`

#### Ghost
.ink, domains

#### Ampache
.kiwi
`installampache`

#### ownCloud
.blue

#### Pydio
.blue

#### SuiteCRM
.red

#### OrangeHRM
.red

### inkVerb special service
These have a flow of their own, are generally used as dependencies, and you should follow their flow to learn more

#### inkCert

#### inkNet


