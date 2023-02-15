# DebianLin-Setup
#
### Install updates
```
sudo apt update
```
#
### Instal [BytzVPN](https://bytzvpn.com/installation.php)

#
### Install Pasword Manager
#
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
### Install git
```
sudo apt install git
```
#
### Install VS Code
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
### Dowload and install latest python version 
1. Install the required dependencies to be able to build Python 3.10 from the source.
   ```
   sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev
   ```
2. Then download Python from the [official Python release page](https://www.python.org/downloads/source/). While on this page, download the Python **Gzippeed tarball**. Alternatively, get the download link and pull it with Wget as shown.
   ```
   wget https://www.python.org/downloads/release/python-3112/Python-3.11.2.tgz
   ```   
3. With the tarball downloaded, extract it as below.
   ```
   tar -xf Python-3.10.*.tgz
   ```
4. Navigate into the extracted directory and run the configure command to check if the required dependencies are available. In the command, the –enable-optimizations flag is used to optimize the binary and run multiple tests
   ```
   cd Python-3.10.*/
   ./configure --enable-optimizations
   ```
5. When the check is complete, build Python 3.10 from the source as below. Remember to speed up the process by using the `-j` flag. This specifies the number of cores in your system. `nproc` command shows your system cores.
   ```
   make -j 4
   ```
6. When make is complete, proceed and install Python 3.10 on Debian 11|10 as below.
   ```
   sudo make altinstall
   ```
   The altinstall flag is used to maintain the default Python binary path in /usr/bin/python.
7. Verify your installation.
   ```
   python3.11.2 --version
   ```
[***Install Python Modules & Create a Python Virtual Environment***](https://computingforgeeks.com/how-to-install-python-on-debian-linux/).
#
### Install LedgerLive
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
5. Launch the AppImage via your terminal:
   ```
   ./ledger-live-desktop-*.AppImage
   ```
   **Note:** in case you get a **sandboxing error**, please run the following command: 
   ```
   ./ledger-live-desktop-*.AppImage --no-sandbox
   ```
#
 ### Install Brave Browser
 
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



