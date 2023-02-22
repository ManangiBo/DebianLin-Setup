# Linux Terminal 
To open Terminal use SHORTCUT: Ctrl+Alt+T
#
**1. Locate and backup bash file**
Before you make any changes, go to your `home directory` and backup the `.bashrc` file. Note taht all files starting with a `.` are invisibil wit the `ls` command, to list hidden files type `la`or `ls -a`. 


after you located your `.bashrc`file type the following command to make a copy for backup purboses: 
```
cp .bashrc bashrc.backup
```
this step is not necessary but if you unsure about what you are doing a backup is always a good place to go back to, if things go wrong.
# 
## Oh-My-Posh
   - [Install OhMyPosh](https://calebschoepp.com/blog/2021/how-to-setup-oh-my-posh-on-ubuntu/)
       ```
       sudo wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh
       sudo chmod +x /usr/local/bin/oh-my-posh
       ``
       These files will be saved under:`/usr/Local/bin/oh-my-posh
   - Download the themes
        ```
        mkdir ~/.poshthemes
        wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/themes.zip -O ~/.poshthemes/themes.zip
        unzip ~/.poshthemes/themes.zip -d ~/.poshthemes
        chmod u+rw ~/.poshthemes/*.json
        rm ~/.poshthemes/themes.zip
        ```
       These files will be saved under:`/home/user/.poshthemes
#
## Fonts
2. **Download and setup [Nerd Fonds](https://www.nerdfonts.com/font-downloads)**
   - Click to: [Download MesloLG Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.3.3/Meslo.zip).

        ```
        cd ~
        mkdir .fonts
        unzip ~/Downloads/Meslo.zip -d ~/.fonts/Meslo
        fc-cache -fv
        ```
4. **Add Posh-Theme to your `PATH` and to your bash shell profile script, `~/.profile` on Debian/Ubuntu**
   - Open .bashrc and .profile files:
       ```
       gedit .bashrc
       gedit .profile
       ```
   - Add the following command to the `.bashrc`file
     ```
     eval "$(oh-my-posh --init --shell bash --config ~/.poshthemes/{theme}.omp.json)"

   - Check path:
     ```
     echo $PATH
     ```
#
3. Install zshell
 
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

     ```
     
    
