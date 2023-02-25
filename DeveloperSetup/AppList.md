## Install latest python version 
 Bash script that downloads Python 3.11.2 from the specified URL, installs it, and adds it to the system PATH:
 ```
#!/bin/bash

url='https://www.python.org/ftp/python/3.11.2/Python-3.11.2.tgz'
output_path='/tmp/Python-3.11.2.tgz'

# Check for dependencies
echo "Checking for required dependencies..."
if ! dpkg -s build-essential zlib1g-dev libffi-dev libssl-dev libreadline-dev libncurses-dev libsqlite3-dev libgdbm-dev libbz2-dev > /dev/null 2>&1; then
    echo "One or more required dependencies are missing. Installing dependencies..."
    sudo apt-get update
    sudo apt-get install -y build-essential zlib1g-dev libffi-dev libssl-dev libreadline-dev libncurses-dev libsqlite3-dev libgdbm-dev libbz2-dev
else
    echo "All required dependencies are already installed."
fi

# Download Python
wget $url -O $output_path

# Extract Python
tar -xf $output_path -C /tmp/
cd /tmp/Python-3.11.2/
./configure
make -j $(nproc)
sudo make install

# Add Python to PATH
echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

echo "Python 3.11.2 has been installed and added to PATH."
```
This script downloads the Python 3.11.2 source code from the specified URL, extracts it to /tmp/Python-3.11.2/, configures the build options, builds Python with multiple threads, installs Python to /usr/local/, adds /usr/local/bin to the system PATH by appending to ~/.bashrc, and sources ~/.bashrc to update the current session's PATH.


You can save this script to a file with the extension .sh (e.g. install-python.sh), make it executable with chmod +x install-python.sh, and run it from the terminal by navigating to the directory where you saved the file and running ./install-python.sh. After running the script, Python 3.11.2 should be installed on your system and accessible from any terminal session.
#
