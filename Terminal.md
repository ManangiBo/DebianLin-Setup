# Linux Terminal 
To open Terminal use SHORTCUT: Ctrl+Alt+T
#
**1. Locate and backup bash file**
[Source](https://www.youtube.com/watch?v=jS-QZKjAd-U)
Before you macke any changes, go to your home directory and backup the .bashrc file. Note taht all files starting with a `.` are invisibil wit the `ls` command, to list hidden files type `ls -a`. 

after you located your .bashrc file type the following command to make a copy for backup purboses: 
```
cp .bashrc bashrc.backup
```
this step is not necessary but if you unsure about what you are doing a backup is always a good place to go back to if things go wrong.

Go to GitHub andersongora/[synth-shell](https://github.com/andresgongora/synth-shell)
#
**2. Install Homebrew**
     ```
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
     ```
   - Add Homebrew to your `PATH` and to your bash shell profile script, `~/.profile` on Debian/Ubuntu
     ```
     test -d ~/.linuxbrew && eval "$(~/.linuxbrew/bin/brew shellenv)"
     ```
     ```
     test -d /home/linuxbrew/.linuxbrew && eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
     ```
     ```
     test -r ~/.profile && echo "eval \"\$($(brew --prefix)/bin/brew shellenv)\"" >> ~/.profile
     ```
     ```
     echo "eval \"\$($(brew --prefix)/bin/brew shellenv)\"" >> ~/.profile
     ```
    The installation script installs Homebrew to `/home/linuxbrew/.linuxbrew` using sudo
   
     
#
**3. Install zshell
 
     ```
     sudo apt install zsh
     ```
   - Change default shell to zshell
     ```
     chsh
     ```
   - Type `/bin/zsh` Enter
    
   - Reboot sesion
   - By opening up the terminal you will be created with the Z Shell configuration function type `2`
#
**4. [Install oh-my-posh](https://ohmyposh.dev/docs/installation/linux)**
   - Install curl
     ```
     sudo apt install curl
     ```
   - Installer
     ```
     sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)
     ```
     
    
