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
#
## Hardware and sensors

### [Read Temperature Sensor and chip Data](https://www.cyberciti.biz/faq/howto-linux-get-sensors-information/)


Installing lm-sensors on a Debian. Type the following:
```
sudo apt-get install lm-sensors
```
### Configuer lm_sensors
To detect hardware monitoring chips, type the following command as the root user:
```
sudo sensors-detect
```

Read sensors chip data such as temperature and fan speed,
Type the following command at shell prompt:
```
sensors
```
> After going thrugh this process temperature shuld show up in Conky.


Watch your sensors data in real time
Type the following watch command:
```
watch -d sensors
```
#

