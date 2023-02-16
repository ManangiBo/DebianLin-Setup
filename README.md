# DebianLin-Setup
#
### Install updates
```
sudo apt update
```
#
### Install [gedit](https://installati.one/debian/11/gedit/)
   ```
   Sudo apt -y install gedit
   ```
#
### Install git
   ```
   sudo apt install git
   ```
#
### Instal [BytzVPN](https://bytzvpn.com/installation.php)
[check video](https://www.youtube.com/watch?v=aWRbs07z9Po)


[check FAQ](https://brax.me/prod/console.php)

Help for MXLinux installing BytzVPN  

.
1. Install the OpenVPN client in the following way depending on what version of Linux you're using.

$ sudo apt install openvpn #Ubuntu/Debian
$ sudo yum install openvpn #CentOS 8/7/6
$ sudo dnf install openvpn #Fedora 22+/CentOS 8

2. When on desktop, you'll have to install the network-manager-openvpn package to change VPN settings via a GUI.

$ sudo yum install network-manager-openvpn #CentOS 8/7/6
$ sudo apt install network-manager-openvpn #Ubuntu/Debian
$ sudo dnf install network-manager-openvpn #Fedora 22+/CentOS 8

3. Once you install the packages, start up OpenVPN to make sure it works properly. Then enable it so that it starts automatically upon startup, thus eliminating the need to start from scratch and re-enter credentials upon each startup. Check its status too.

$ sudo systemctl start openvpn
$ sudo systemctl enable openvpn
$ sudo systemctl status openvpn

4. Next you'll need to import the .ovpn profile for whichever region you select.

$ cd ~
$ scp [insert profile name here]

5. Go to system Settings and then Network. Click the plus sign next to VPN.

6. In the next window, click "import from profile" and select the .ovpn file of the profile you want.

7. For non-Ubuntu systems, click on the network settings in system, check Network Connections, then click the plus sign to create a new connection. Select "Import a saved VPN configuration..." and press "Create".

8. After importing the .ovpn file, viewing the settings, and importing the credentials from Settings>My Account Settings>View VPN Credentials (on Brax.Me) click "Add".

9. Once you import it successfully, activate the OpenVPN under "Network".

10. Use $ip add to view the network tunnel interface for the newly installed VPN.






#
### Install Pasword Manager
#
### Setup Email client
    Install
    ```
    sudo apt install kmail
    ´´´
    
    
    
    
### Configure firewall
UFW, or Uncomplicated Firewall, provides an easy to use interface for inexperienced Linux users to set up the Linux firewall.


1. Install Debian UFW by running the command:
   ```
   sudo apt-get install ufw -y
   ```
2. Start UFW service and enable it to start on boot time by running the following linux command:
   ```
   sudo ufw enable
   ```
3. Check the status of UFW:
   ```
   apt ufw status
   ```
   You shuld see the output: `Status: active`
   
   
4. disable UFW firewall:
   ```
   apt ufw disable
   ```
#
## Install VS Code
The easiest and recommended way to install Visual Studio Code on Debian 10 systems is to enable the VS Code repository and install the VS Code package through the command line:


1. Install dependencies required:
   ```
   sudo apt install gnupg2 software-properties-common apt-transport-https curl
   ```
2. Import Microsoft’s GPG key using the following curl command:
   ```
   curl -sSL https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
   ```
   On success, the command will return `OK`.

3. Add the Visual Studio Code repository to your system:
   ```
   sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
   ```

4. Once you’ve enabled the repository, update the system and install Visual Studio Code by running the command:

   ```
   sudo apt update
   ```
   ```
   sudo apt install code
   ```
#
[***Install Python Modules & Create a Python Virtual Environment***](https://computingforgeeks.com/how-to-install-python-on-debian-linux/).
#
#
## Install LedgerLive
       ![Ledger Logo](https://i1.wp.com/www.uniquenewsonline.com/wp-content/uploads/2021/03/Ledger-live.png?resize=768%2C432&ssl=1)

1. Navigate to [Ledger-live Downloads](https://www.ledger.com/ledger-live).
2. Download the Ledger Live AppImage.
3. in the terminal move to the download folder and make the file executable: 
   ```
   chmod +x ledger-live-*.AppImage
   ```
4. Enter the following command to automatically add the udev rules and reload udev to allow USB access to your Ledger device:
   ```
   wget -q -O - https://raw.githubusercontent.com/LedgerHQ/udev-rules/master/add_udev_rules.sh | sudo bash
   ```
   **Note**: New versions of Ubuntu 22.04 LTS require adding the following commands after **wget**:

   `sudo add-apt-repository universe`
   `sudo apt install libfuse2`___(3-3)___
   
   
5. Extract icon file and .desktop file
   ```
   Cd ~/Downloads
   ./ledger-live*.AppImage --appimage-extract
   ```
   This creates the folder `squashfs-root`
   
6. Make `icons` and `applications` directorys(if not already ins /usr/share)
   ```
   sudo mkdir -p /usr/share/icons
   ```
   ```
   sudo mkdir -p /usr/share/applications
   ```
   
7. Copy files to the share folder
   ```
   sudo cp ledger-live*.desktop /usr/share/applications
   ```
   ```
   sudo cp ledger-live*.png /usr/share/icons
   ``` 
8. navigate to .desktop file
   ```
   cd /usr/share/applications
   ```
9. Edit the .desktop file
   ```
   sudo gedit ledger-live-desktop.desktop
   ```
   ***Note:***`ǵedit` needs to be installed(see top)
   
   
   In the ledger live desktop.desktop file, find `Èxec=`and type the full path of the Ledger-Live-Desktop location.
   
   
10. Optional launch the AppImage via your terminal:
   ```
   ./ledger-live-desktop-*.AppImage
   ```
   **Note:** in case you get a **sandboxing error**, please run the following command: 
   ```
   ./ledger-live-desktop-*.AppImage --no-sandbox
   ```
#
#
 ## Install Brave Browser
 
1. You need the curl function installed, to do so run the command:
   ```
   sudo apt install curl
   ```
2. key
```
`  sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-          release.s3.brave.com/brave-browser-archive-keyring.gpg
   ```
3. Echo
```
`  echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list
```
  
4. Update
   ```
   `sudo apt update
   ```
5. Install 
   ```
   sudo apt install brave-browser
   ```
### Browser setup
***Extentions***
  - Authenticator - 2 Factor for websites
  - Click and Clean - History and Cache cleaning
  - GoFullPage - Full Page Screen Capture
  - Bitwarden - Password Management 
  - Web Highlights - Highlight parts of a webpage
  - MetaMask - Wallet
  - Phantom - Wallet 
  - Midnight Lizard - Dark mode everywhere
  - Momentum
[***Backup***](https://www.addictivetips.com/ubuntu-linux-tips/back-up-the-brave-browser-profile/)
# 
### Install [Quickemu](https://github.com/quickemu-project/quickemu) vertual 
1. Install dependencies for Debian System 
```
   sudo apt install qemu bash coreutils ovmf grep jq lsb procps python3 genisoimage usbutils util-linux sed spice-client-gtk swtpm wget xdg-user-dirs zsync unzip
```

#
### Speed up the boot time
The default settings for the GRUB timeout menu selection during the system boot is 5 seconds. To change this value, 


1. open the GRUB configuration file by using the following command:
   ```
   sudo nano /etc/default/grub
   ```
2. Change the delay value to 0 seconds, by setting `GRUB_TIMEOUT=0:`
Once you are done, press `Ctrl+O` and `Ctrl+X` to save and exit 
3. Then update your GRUB settings by using the command:
   ```
   sudo update-grub
   ```
`



