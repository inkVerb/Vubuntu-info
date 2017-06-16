# GitHub

## Update an existing repo from the command line
cd [dir]
git add .
git commit -m "Update"
git push -u origin master

## Two URL Styles:
### HTTPS:
https://github.com/inkVerb/YourRepo.git
### SSH:
git@github.com:inkVerb/YourRepo.git

## Clone to local machine
### HTTPS:
git clone https://github.com/inkVerb/YourRepo.git
### SSH:
git clone git@github.com:inkVerb/YourRepo.git

## Add existing repo (With README.md all setup)
### Create the repo "inkVerb/YourRepo" on GitHub (DO NOT initiate with README.md !!!)
### Initiate it from your local computer
cd [dir]
git init
git add .
git commit -m "First commit"
git remote add origin URL
git remote -v
git push origin master

## Create New Repo via command Line
### Create the repo "inkVerb/YourRepo" on GitHub (DO NOT initiate with README.md !!!)
### Initiate it from your local computer
echo "# YourRepo" >> README.md
git init
git add .
git commit -m "First commit"
git remote add origin URL
git push -u origin master

## Push an existing repo from the command line
git remote add origin URL
git push -u origin master

## Setup Git local user info
### Global
git config --global user.name "MonaLisa"
git config --global user.name
#### Confirm ###
git config --global user.email "email@example.com"
git config --global user.email
#### Confirm ###
### Individual
cd [specific directory of repo]
git config user.name "MonaLisa"
git config user.name
#### Confirm ###
git config user.email "email@example.com"
git config user.email
#### Confirm ###


## Setup Git SSH keys ## Optional!
### Create ssh keys (-N "" for no passphrase, -f /path/to/KEYNAME)
ssh-keygen -t rsa -N "" -f ~/.ssh/GitHub
### Find the public key to copy-paste
cat ~/.ssh/GitHub.pub
### Add the key on Github
#### >GitHub Avatar > Settings > SSH and GPG keys + New/Add SSH key
### Do a test on your machine (Necessary)
ssh -T git@github.com
