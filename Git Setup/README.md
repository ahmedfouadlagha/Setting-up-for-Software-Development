# Git Setup
## Installing Git
[download](https://git-scm.com/downloads)
## Configuring Terminal
1. download the zipped file from [here](https://github.com/ahmedfouadlagha/Setup/blob/main/ud123-udacity-terminal-config.zip)
2. move the directory udacity-terminal-config to your home directory and name it .udacity-terminal-config (there's a dot at the front, now!)
3. move the bash_profile file to your home directory and name it .bash_profile (there's a dot at the front, now!)
    > if you already have a .bash_profile file in your home directory, transfer the content from the downloaded bash_profile to your existing .bash_profile

## First Time Git Configuration

**sets up Git with your name**
    
    git config --global user.name "<Your-Full-Name>"

**sets up Git with your email**
    
    git config --global user.email "<your-email-address>"

**makes sure that Git output is colored**
    
    git config --global color.ui auto

**displays the original state in a conflict**
    
    git config --global merge.conflictstyle diff3
    git config --list

## Git & Code Editor
**Atom Editor Setup**
    
    git config --global core.editor "atom --wait"
    
**Sublime Text Setup**
    
    git config --global core.editor "'C:/Program Files/Sublime Text 2/sublime_text.exe' -n -w"
    
**VSCode Setup**

    git config --global core.editor "code --wait"
