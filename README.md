# xlxd-debian-installer (Debian 11 Support!)
## M0VUB Fork - N5AMD 
With thanks!

This script simply runs through the official install instructions found [HERE](https://github.com/LX3JL/xlxd). The script will install XLX along with setting up the web dashboard to view real-time activity. After installing this you will have a private or public D-Star, DMR, and YSF XLX Reflector.

At the start of 2020 a new version of XLX was released that allows for native C4FM connections. This means it's even simpler to run a multi-mode reflector. XLX now natively supports DMR, D-Star, and C4FM. C4FM and DMR do not require any transcoding hardware (AMBE) to work together. If you plan on using D-Star with any of the other modes, you will need hardware AMBE chips.

### New Features 2021
1. Ubuntu / Debian 11 support
2. Edit configuration during install
3. HTTPS / SSL Auto Support (Certbot) Debian 11
5. Support for IMRS
6. Support for G3 Terminal Mode

### To Install:
1. Have a fresh Debian 9 10 OR 11 computer ready and up to date.
2. Have both a FQDN and 3 digit XLX number in mind before beginning.
3. 
```sh
git clone https://github.com/ShaYmez/xlxd-debian-installer
cd xlxd-debian-installer
./xlxd-debian-installer.sh
```
### Edit main.h
During the install proccess you will be asked to edit main.h. This is where you can configure your MAX amount of modules and YSF reflector automation. If you are unfamiliar with this just simply "CONTL-X", hit "Y" and and the install proccess will automatically continue.
## HTTPS / SSL support (Debian 11)
A new feature in this script is the HTTPS / SSL certbot script. This is automatic. You will be prompted with info, just follow the on screen instructions. It is not required to have the dashboard SSL secured but is recommended! (Keep your browser happy!)
## How to find what reflectors are available
Find a current active reflector dashboard, for example, https://xlx.n5amd.com/index.php?show=reflectors and you will see the gaps in reflector numbers in the list. Those reflector numbers not listed are available. 

### To interact with xlxd after installation:
```sh
systemctl start|stop|status|restart xlxd
```
 - Installs to /xlxd
 - Logs are in /var/log/messages and *'systemctl status xlxd'*
 - Main config file is /var/www/xlxd/pgs/config.inc.php
 - You will need to edit config.inc.php to enable public reflector'**
 - Be sure to restart xlxd after each config change *'systemctl restart xlxd'*

**For more information, please visit:**

https://n5amd.com/digital-radio-how-tos/create-xlx-xrf-d-star-reflector/
