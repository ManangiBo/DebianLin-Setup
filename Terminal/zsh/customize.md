install zsh using: 
```
sudo apt-get -y install zsh
```
Once the installation completes, you can check the version using `zsh --version`, then make zsh your default shell using `chsh -s /bin/zsh`. You’ll need to log out, then log back in for the changes to take effect.


Optional, to find out what shells a currently installed n the system type:
```
cat /etc/shells
```
to find out more details about your currend shell, type:
```
$USER /etc/passwd
```
#
Open `.zshrc` file in VS code 
```
cd ~
code .zshrc
```
#
Install [exa](https://the.exa.website) command
```
apt install exa
```
#
Enter the following Aliases on the bottom of the file 
```
# Aliases
alias zshconfig="code ~/.zshrc"
alias ohmyzsh="code ~/.oh-my-zsh"
alias install="sudo apt-get install"
alias myip='curl http://ipecho.net/plain; echo'
alias distro='cat /etc/*-release'
alias reload='source ~/.zshrc'
alias sapu='sudo apt-get update'
alias ffs='sudo !!'
alias y='yarn'
alias zshconfig='subl $HOME/.zshrc'
alias remove="sudo apt-get remove --purge"
alias myip="curl http://ipecho.net/plain; echo"
alias la='exa --icons -a --classify'
alias lla='exa --header --long --icons -a --classify'
alias ls='exa --icons --classify'
alias ll='exa --header --long --icons --classify'
alias lg='exa --long --git'

# zsh config dir
# export ZDOTDIR=$HOME/.config/zsh

```
Apply the changes: `source ~/.zshrc` or `. ~/.zshrcor` or you can restart your terminal session.
#
Plugins:
[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
[Fig](https://fig.io/download)
sudo


