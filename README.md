# Git Setup
## Installing Git
[download](https://git-scm.com/downloads)
## Configuring Terminal
1. Clone the repository to your local machine:
   ```sh
   $ git clone https://github.com/ahmedfouadlagha/Setting-up-for-Software-Development.git ~/
   ```
2. move the directory terminal-config to your home directory and name it .terminal-config (there's a dot at the front, now!)
   ```sh
   $ cd
   $ start .
   $ mv terminal-config .terminal-config
   ```
3. move the bash_profile file to your home directory and name it .bash_profile (there's a dot at the front, now!)
    > if you already have a .bash_profile file in your home directory, transfer the content from the downloaded bash_profile to your existing .bash_profile
   ```sh
   $ mv bash_profile .bash_profile
   ```

## First Time Git Configuration

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
   $ git config --list
   ```   
## Git & Code Editor
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
    
