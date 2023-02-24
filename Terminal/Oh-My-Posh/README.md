#Oh-My-Posh
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
       ```
       These files will be saved under:`/usr/Local/bin/oh-my-posh`
       
       
   - Download the themes(optional)
        ```
        mkdir ~/.poshthemes
        wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/themes.zip -O ~/.poshthemes/themes.zip
        unzip ~/.poshthemes/themes.zip -d ~/.poshthemes
        chmod u+rw ~/.poshthemes/*.json
        rm ~/.poshthemes/themes.zip
        ```
       These files will be saved under:`/home/user/.poshthemes`
       
    
   - Alternatively you can crate your own folder were you can pull themes from GitHub into or create your own (just make sure that when you add themes to your PATH later on that you chose this folder)
       ```
       cd ~
       mkdir .Poshthemes
       ```
#
## Fonts
   - Download and setup [Nerd Fonds](https://www.nerdfonts.com/font-downloads)
   - Click to: [Download MesloLG Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.3.3/Meslo.zip). or 
   - [Download Hack Nerd Fonts](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.3.3/Hack.zip)

        ```
        cd ~
        mkdir .fonts
        unzip ~/Downloads/Meslo.zip -d ~/.fonts/Meslo
        fc-cache -fv
        ```
   **Note**:The fc-cache command is used to build font information cache files that are used by fontconfig library to efficiently access font files. The -f option is used to force a re-cache, even if no changes have been made to the font directories since the last time they were cached. The -v option is used to show verbose output, displaying the names of the font files as they are being cached.

So, the fc-cache -fv command will force fontconfig to rebuild the font information cache files for all installed fonts, displaying the name of each font file as it is being cached.
 #
 ## Add Oh-My-Posh and Themes to PATH
 **Add Posh-Theme to your `PATH` and to your bash shell profile script, `~/.profile` on Debian/Ubuntu**
   - Open .bashrc and .profile files:
       ```
       gedit .bashrc
       gedit .profile
       ```
   - Add the following command to the `.bashrc`file
       ```
       eval "$(oh-my-posh --init --shell bash --config ~/.poshthemes/{theme}.omp.json)"
       ```
   - Check path:
       ```
       echo $PATH
       ```
#
## Setup new default profile using the installed Font
  - Go to `Preferences` in the dropdown manue in the top right corner of your shell windwo.
  - Click on The **+** next to Profile
  - Turn Custom Fonds on 
  - Chose your prefered font (MesloGS NF Regular in this example)
  - Click on the arrow next to your New Profile Name and select `set as default`
#
## Create and eddit .json file 
     ´´´
     cd ~/.poshthemes
     touch ManangiLinTerm.omp.json
     code ManangiLinTerm.omp.json
     
     ```
