# Setting up for Software Development
## System preparation and cleanup
1. Windows Update
```powershell
Enable-MicrosoftUpdate
Install-WindowsUpdate -acceptEula
```
2. Go to Task manager > startup apps > Disable all applications
3. windows key > parameters > Apps > Startup > Disable all applications
4. windows key > power options > set to balance >> change plan settings
5. Optimizing Performance
```
powercfg -duplicatescheme 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c
```
or 
```
powercfg /s SCHEME_MIN
```
6. go back to power options, now high Performance is enabled
7. windows key > parameters > Apps > installed apps > uninstall unnecessary apps
8. windows key > visual effects > off every things
9. personalization > colors > transparency effects > off
10. windows key > view advanced system settings > Performance options (settings) > adjust for best performance
11. windows key > notifications
## Preparing the command line
```
Set-ExecutionPolicy Unrestricted
```
## Installing Windows Subsystem for Linux (WSL)
### 1. Setting up WSL and virtualization
- Windows key + R
- `optionalfeatures.exe` and hit enter
- search for `Windows Subsystem for Linux` and activate it > ok
### 2. Ubuntu install
Open PowerShell or Windows Command Prompt in **administrator** mode
```powershell
wsl --install
```
### 3. Ubuntu configuration
1. Open PowerShell or Windows Command Prompt in **administrator** mode
```powershell
ubuntu config --default-user root
```
2. open ubuntu terminal
```
sudo apt update
sudo apt install build-essential
```
## Winget
visit the website : [here](https://winget.run/)
## Git Setup
### 1. Installing Git
you can download it and install it from [here](https://git-scm.com/downloads) or execute the following command
```powershell
winget install -e --id Git.Git
```
### 2. First Time Git Configuration
**sets up Git with your name**
   ```sh
   $ git config --global user.name "<Your-Full-Name>"
   ```
**sets up Git with your email**
   ```sh
   $ git config --global user.email "<your-email-address>"
   ```
**makes sure that Git output is colored**
   ```sh
   $ git config --global color.ui auto
   ```
**displays the original state in a conflict**
   ```sh
   $ git config --global merge.conflictstyle diff3
   ```
**show configuration**
   ```sh
   $ git config --list
   ```
### 3. Git & Code Editor
**Atom Editor Setup**
   ```sh
   $ git config --global core.editor "atom --wait"
   ```    
**Sublime Text Setup**
   ```sh
   $ git config --global core.editor "'C:/Program Files/Sublime Text 2/sublime_text.exe' -n -w"
   ```     
**VSCode Setup**
   ```sh
   $ git config --global core.editor "code --wait"
   ```
## VS Code
```
winget install -e --id Microsoft.VisualStudioCode
```
## Visual Studio Community Edition 
- download from [here](https://www.microsoft.com/en-us/download/details.aspx?id=104781)
- select "ASP.NET" + AZURE + .NET Multi + .NET desktop
## SQL Server Express
- download from [here](https://www.microsoft.com/fr-fr/download/details.aspx?id=104781)
- basic is fine
## SSMS
- install ssms

## Docker
- download from [here](https://www.docker.com/products/docker-desktop/)
- after installation : settings > resources > wsl intergration > ubuntu enable > apply
## VS Code extensions and Settings Sync

## Node Version Manager (NVM) and NodeJS
1. install curl
```
sudo  apt-get install curl
```
2. install **nvm**
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
nvm install 18
node --version
```
## Python with Conda 
```
$ wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```
### Betty
- Clone the repo to your local machine
```
$ git clone https://github.com/holbertonschool/Betty
```
- `cd` into the `Betty` directory
```
$ cd Betty
```
- Install the linter with `sudo ./install.sh`
```
sudo ./install.sh
```
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
$ mkdir ~/Code
```
## vim/emacs configuration
### vim
```
vi .vimrc
```
----
```
set tabstop=8 shiftwidth=8
set autoindent
set smartindent
set cindent
syntax enable
set number
```
### emacs
```
vi .emacs
```
----
```

	(setq c-default-style "bsd"
      c-basic-offset 8
      tab-width 8
      indent-tabs-mode t)
(require 'whitespace)
(setq whitespace-style '(face empty lines-tail trailing))
(global-whitespace-mode t)
(setq column-number-mode t)
```
## Configuring bash Terminal
1. Clone the repository to your local machine:
   ```sh
   $ git clone https://github.com/ahmedfouadlagha/Setting-up-for-Software-Development.git ~/
   ```
2. move the `.terminal-config` to your home directory
   ```sh
   $ cd
   $ start .
   $ mv .terminal-config ~/
   ```
3. move the `.bash_profile` file to your home directory.
> [!NOTE]
> if you already have a `.bash_profile` file in your home directory, transfer the content from the downloaded bash_profile to your existing `.bash_profile`
   ```sh
   $ mv .bash_profile ~/
   ```
