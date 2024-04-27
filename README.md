# Setting up for Software Development
## System preparation and cleanup
## Optimizing Performance
```
powercfg -duplicatescheme 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c
```
## Preparing the command line
## Installing Windows Subsystem for Linux (WSL)
### 1. Setting up WSL and virtualization
- activate Windows Subsystem for Linux
   - Windows key + R
   - optionalfeatures.exe and hit enter
   - search for `Windows Subsystem for Linux` and activate it > ok
### 2. Ubuntu install
```
wsl --install
ubuntu config --default-user root
sudo apt update
sudo apt install build-essential
```
## Git
```
winget install -e --id Git.Git
git config --global user.name "Ahmed Fouad Lagha"
git config --global user.email "laghaahmedfouad@gmail.com"
```
## Winget
## VS Code
```
winget install -e --id Microsoft.VisualStudioCode
```
## Visual Studio Community Edition 
- click [here](https://www.microsoft.com/en-us/download/details.aspx?id=104781)
- Server=localhost\SQLEXPRESS;Database=master;Trusted_Connection=True;
## SQL Server Express
## SSMS
## Docker
## VS Code extensions and Settings Sync
## Workin inside WSL
## Node Version Manager (NVM) and NodeJS
```
sudo  apt-get install curl
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
nvm install 18
node --version
```
- __NodeJS example:__
## Python with Conda 
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
- __Python example__
### Betty
- Clone the repo to your local machine
```
git clone https://github.com/holbertonschool/Betty
```
- `cd` into the Betty directory (`cd Betty`)
- Install the linter with `sudo ./install.sh`
- `emacs` or `vi` a new file called `betty` (```vi betty```), and copy the script below 
```
#!/bin/bash
# Simply a wrapper script to keep you from having to use betty-style
# and betty-doc separately on every item.
# Originally by Tim Britton (@wintermanc3r), multiargument added by
# Larry Madeo (@hillmonkey)

BIN_PATH="/usr/local/bin"
BETTY_STYLE="betty-style"
BETTY_DOC="betty-doc"

if [ "$#" = "0" ]; then
    echo "No arguments passed."
    exit 1
fi

for argument in "$@" ; do
    echo -e "\n========== $argument =========="
    ${BIN_PATH}/${BETTY_STYLE} "$argument"
    ${BIN_PATH}/${BETTY_DOC} "$argument"
Done
```
- Once saved, exit file and change permissions to apply to all users with `chmod a+x betty`
- Move the betty file into /bin/ directory or somewhere else in your $PATH with `sudo mv betty /bin/`

## dirctory porojects
```
$ mkdir Code
```
## vim configuration
```
vi .vimrc

 set tabstop=8 shiftwidth=8
 set autoindent
 set smartindent
 set cindent
 syntax enable
 set number
vi .emacs

	(setq c-default-style "bsd"
      c-basic-offset 8
      tab-width 8
      indent-tabs-mode t)
(require 'whitespace)
(setq whitespace-style '(face empty lines-tail trailing))
(global-whitespace-mode t)
(setq column-number-mode t)
```
