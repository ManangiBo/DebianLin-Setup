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
