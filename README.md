# Script and instruction for building openFrameworks on C.H.I.P.
Tested with openFrameworks 0.9.8 and CHIP OS 4.4.13

From a freshly flashed chip:

update and upgrade

`sudo apt-get update`

`sudo apt-get upgrade`


install git and clone this repo if not already done

`sudo apt-get install git`

`git clone https://github.com/zealtv/ofInstallChip.git`


cd into repo directory

`cd ofInstallChip`


make excecutable and run the install_dependencies_chip.sh script in this repo - this is the same as the standard install_dependencies script with mesa related packages removed.

`chmod +x ./install_dependencies_chip.sh`

`sudo ./install_dependencies_chip.sh`


download and extract openFrameworks for linux arm7:

`cd where/ever/you/want/to/install/of`

`wget http://openframeworks.cc/versions/v0.9.8/of_v0.9.8_linuxarmv7l_release.tar.gz`

`tar -xf of_v0.9.8_linuxarmv7l_release.tar.gz`


go to script folder 

`cd of_v0.9.8_linuxarmv7l_release/scripts`


install codecs 

`sudo linux/debian/install_codecs.sh`


build openFrameworks 

`sudo ./compileOF.sh`


rebuild poco 

`cd scripts/apothecary`

`./apothecary -tlinuxarmv7l update poco`


Done! Go build an example and test
