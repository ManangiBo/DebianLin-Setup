#
### Download and install
```
sudo apt-get install conky-all
```
> Test: `conky`
#
### extract a config file for conky
Make a direktory for `config` files in your `Documents` folder and extract `conky.conf` into it:
```
mkdir ~/Documents/Config.files
conky -C > ~/Documents/Config.files/conky.conf
```
make directory for `conky.conf` in `~/.config` :
``` 
mkdir ~/.config/conky
```
Open `conky.conf` in VSCode :
```
code ~/Documents/Config.files/conky.conf
```
- Find ·[NEONCiper-Conky.conf](https://github.com/kenpc-git/NEONCipher-Conky.conf-FIXED/blob/main/conky.conf),
- Copy paste the content into the `conky.conf`
- Save and close VSCode 


Back in the terminal Copy `conky.conf` to `~/.config/conky` folder
```
cp -v ~/Documents/Config.files/conky.conf ~/.config/conky
```
> Test: `conky`

