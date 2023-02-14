# DebianLin-Setup
#
### Install updates
```
sudo apt update
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
2. Download [the latest available version of Python](https://www.python.org/downloads/source/).
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


   
   
